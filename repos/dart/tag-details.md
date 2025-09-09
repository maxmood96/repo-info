<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.10.0-162.1.beta`](#dart3100-1621beta)
-	[`dart:3.10.0-162.1.beta-sdk`](#dart3100-1621beta-sdk)
-	[`dart:3.9`](#dart39)
-	[`dart:3.9-sdk`](#dart39-sdk)
-	[`dart:3.9.2`](#dart392)
-	[`dart:3.9.2-sdk`](#dart392-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:cc4d50f840b502dde7068fca505efedad0802817b15b78218b4512396717464a
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
$ docker pull dart@sha256:3e66cf04d5ede710f73734d83c49fe5f598729f668c4405e182642be071633d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295375890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d74785f94badad3736afeb4f7b76e9d43b4857aaafa417cea6b388f06959e30`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Sep 2025 11:42:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05c4aceb529f35f93eb6f1738babefcc3b2a7b2711d60e096f1460aa9f7dbae`  
		Last Modified: Mon, 08 Sep 2025 22:09:12 GMT  
		Size: 42.5 MB (42482593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677702b67ee1965df50e8ff7bab9200d6d743530e36e1b42449bbd70797ed751`  
		Last Modified: Mon, 08 Sep 2025 21:42:42 GMT  
		Size: 1.9 MB (1873612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e8b7557068bfac0eba4dd938e4106f62ce53b7dfe00f994ef29ee540375007`  
		Last Modified: Mon, 08 Sep 2025 22:09:11 GMT  
		Size: 221.2 MB (221246158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:57c77b466c4fdbc8b68d3e27de68f3c1ed005a8578d1337ccb4f79aaf16fc06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494a0f550d210d3f67be8f09d39f230732d45f2693dbb952b6da288add8c5f26`

```dockerfile
```

-	Layers:
	-	`sha256:e35e641e01735e6bbe594b05c7c452e632dd7974107ee3a3e6077d78a6f89af9`  
		Last Modified: Mon, 08 Sep 2025 23:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:34051496922f2a4ede768b1340880bdb586c93b08880e93fa0a9202efd6a385d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220750428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f328cd29cfc7c7bdbebb76a23f626c68f4dacf31e7ad16d3e00dad21f5437e`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56836f0c8e8c91ed8d9b18dcd856474127d1246651d41c7a7e1d85c5aa587e7`  
		Last Modified: Mon, 08 Sep 2025 23:12:50 GMT  
		Size: 37.5 MB (37478354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55445b8ad1d9275c46905f2852157c3dea0ba0d8318f4165761fdbc4a4d1804f`  
		Last Modified: Mon, 08 Sep 2025 22:47:12 GMT  
		Size: 1.3 MB (1275112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836ea90eeff7caed8d596d2ebd8d662040dac66c7d25e191612897e12c08911d`  
		Last Modified: Mon, 08 Sep 2025 23:12:42 GMT  
		Size: 155.8 MB (155789083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:0df9580b782efa5922674f248545627fa84db083825a4e488475bc2c245b2a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391e8aae71d36fc2f2abf20bf2fff2f507db492df051c3d7b57117589ed3c492`

```dockerfile
```

-	Layers:
	-	`sha256:061e9d6d0f6c9b75254d85de65985c3e07a743a84cda822a5ffb31980d39df13`  
		Last Modified: Mon, 08 Sep 2025 23:53:26 GMT  
		Size: 20.8 KB (20804 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:a97c783bb9e61ae8e7c7f8038e236fc6150abe9eca36ff0edaee0aee8b70920c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294659560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b214cc2238e49e232fecafca40cee02d5cfb266fc3faf3db364061d70b51e31`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c190eda88054318fcbdee78d8ef8cae137f19117a7e2bec8cc689ce5b64343`  
		Last Modified: Mon, 08 Sep 2025 23:53:48 GMT  
		Size: 42.3 MB (42270213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29205cde420f3386a6ec932407c0e575887fc341ae65db74ea280da3c6623f5`  
		Last Modified: Mon, 08 Sep 2025 22:25:11 GMT  
		Size: 1.6 MB (1566648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b121f20624a7437e0ea7c95f071379390a425cf722473abab14cd23cb34732`  
		Last Modified: Mon, 08 Sep 2025 23:53:51 GMT  
		Size: 220.7 MB (220686036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:297f008f6b5a02b796303bcff9642a65fd7849749ea887ccf39e3d8addc47ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c61a8b35b2aa67809ba8bdcc5eb7a48c23ea623044e44a13278599ea4374ee`

```dockerfile
```

-	Layers:
	-	`sha256:9a072058476f89d2d11b4b1e8f47b1501e0c353ae192e8928ecff1a605717089`  
		Last Modified: Mon, 08 Sep 2025 23:53:29 GMT  
		Size: 20.9 KB (20855 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; riscv64

```console
$ docker pull dart@sha256:a23a20664bad82073426026d01cd12f3f78729248a9a2b7fb3a1c3d7cfb709d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232352464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db3501795667e769c99accfe9399dd1d60358614edcd0644c96f5b1f122a121`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 27 Aug 2025 13:56:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 27 Aug 2025 13:56:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Aug 2025 13:56:45 GMT
WORKDIR /root
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f4927a3b04f70ec84088797f16339585618b2ec5aa5be4346e1db849de61a9`  
		Last Modified: Fri, 22 Aug 2025 03:19:46 GMT  
		Size: 41.5 MB (41549900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c103a39452af771458a8486e75d619bd52bca9bbf9f861f226f97afc19e70413`  
		Last Modified: Fri, 22 Aug 2025 03:19:42 GMT  
		Size: 1.6 MB (1567069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddcc9f0e9b433e088c2545cbd386786132bc494afa98bbf9cceb57617d2d367`  
		Last Modified: Fri, 29 Aug 2025 14:11:28 GMT  
		Size: 161.0 MB (160963840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:bce66f6d4297b47739c0954c0afb8a0d7ce89f167c49c26bb1aeb3183b4178d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d2a55131dba91a6d7993453feca1bc13eb3c878c7a270118bccf37a300adc0`

```dockerfile
```

-	Layers:
	-	`sha256:0082cc5e010b406fa5e9b523d55c695237a6177c1d766f114194870d8bf70c8e`  
		Last Modified: Fri, 29 Aug 2025 14:53:23 GMT  
		Size: 20.7 KB (20733 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:cc4d50f840b502dde7068fca505efedad0802817b15b78218b4512396717464a
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
$ docker pull dart@sha256:3e66cf04d5ede710f73734d83c49fe5f598729f668c4405e182642be071633d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295375890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d74785f94badad3736afeb4f7b76e9d43b4857aaafa417cea6b388f06959e30`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Sep 2025 11:42:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05c4aceb529f35f93eb6f1738babefcc3b2a7b2711d60e096f1460aa9f7dbae`  
		Last Modified: Mon, 08 Sep 2025 22:09:12 GMT  
		Size: 42.5 MB (42482593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677702b67ee1965df50e8ff7bab9200d6d743530e36e1b42449bbd70797ed751`  
		Last Modified: Mon, 08 Sep 2025 21:42:42 GMT  
		Size: 1.9 MB (1873612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e8b7557068bfac0eba4dd938e4106f62ce53b7dfe00f994ef29ee540375007`  
		Last Modified: Mon, 08 Sep 2025 22:09:11 GMT  
		Size: 221.2 MB (221246158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:57c77b466c4fdbc8b68d3e27de68f3c1ed005a8578d1337ccb4f79aaf16fc06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494a0f550d210d3f67be8f09d39f230732d45f2693dbb952b6da288add8c5f26`

```dockerfile
```

-	Layers:
	-	`sha256:e35e641e01735e6bbe594b05c7c452e632dd7974107ee3a3e6077d78a6f89af9`  
		Last Modified: Mon, 08 Sep 2025 23:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:34051496922f2a4ede768b1340880bdb586c93b08880e93fa0a9202efd6a385d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220750428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f328cd29cfc7c7bdbebb76a23f626c68f4dacf31e7ad16d3e00dad21f5437e`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56836f0c8e8c91ed8d9b18dcd856474127d1246651d41c7a7e1d85c5aa587e7`  
		Last Modified: Mon, 08 Sep 2025 23:12:50 GMT  
		Size: 37.5 MB (37478354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55445b8ad1d9275c46905f2852157c3dea0ba0d8318f4165761fdbc4a4d1804f`  
		Last Modified: Mon, 08 Sep 2025 22:47:12 GMT  
		Size: 1.3 MB (1275112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836ea90eeff7caed8d596d2ebd8d662040dac66c7d25e191612897e12c08911d`  
		Last Modified: Mon, 08 Sep 2025 23:12:42 GMT  
		Size: 155.8 MB (155789083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0df9580b782efa5922674f248545627fa84db083825a4e488475bc2c245b2a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391e8aae71d36fc2f2abf20bf2fff2f507db492df051c3d7b57117589ed3c492`

```dockerfile
```

-	Layers:
	-	`sha256:061e9d6d0f6c9b75254d85de65985c3e07a743a84cda822a5ffb31980d39df13`  
		Last Modified: Mon, 08 Sep 2025 23:53:26 GMT  
		Size: 20.8 KB (20804 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:a97c783bb9e61ae8e7c7f8038e236fc6150abe9eca36ff0edaee0aee8b70920c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294659560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b214cc2238e49e232fecafca40cee02d5cfb266fc3faf3db364061d70b51e31`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c190eda88054318fcbdee78d8ef8cae137f19117a7e2bec8cc689ce5b64343`  
		Last Modified: Mon, 08 Sep 2025 23:53:48 GMT  
		Size: 42.3 MB (42270213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29205cde420f3386a6ec932407c0e575887fc341ae65db74ea280da3c6623f5`  
		Last Modified: Mon, 08 Sep 2025 22:25:11 GMT  
		Size: 1.6 MB (1566648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b121f20624a7437e0ea7c95f071379390a425cf722473abab14cd23cb34732`  
		Last Modified: Mon, 08 Sep 2025 23:53:51 GMT  
		Size: 220.7 MB (220686036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:297f008f6b5a02b796303bcff9642a65fd7849749ea887ccf39e3d8addc47ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c61a8b35b2aa67809ba8bdcc5eb7a48c23ea623044e44a13278599ea4374ee`

```dockerfile
```

-	Layers:
	-	`sha256:9a072058476f89d2d11b4b1e8f47b1501e0c353ae192e8928ecff1a605717089`  
		Last Modified: Mon, 08 Sep 2025 23:53:29 GMT  
		Size: 20.9 KB (20855 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:a23a20664bad82073426026d01cd12f3f78729248a9a2b7fb3a1c3d7cfb709d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232352464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db3501795667e769c99accfe9399dd1d60358614edcd0644c96f5b1f122a121`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 27 Aug 2025 13:56:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 27 Aug 2025 13:56:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Aug 2025 13:56:45 GMT
WORKDIR /root
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f4927a3b04f70ec84088797f16339585618b2ec5aa5be4346e1db849de61a9`  
		Last Modified: Fri, 22 Aug 2025 03:19:46 GMT  
		Size: 41.5 MB (41549900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c103a39452af771458a8486e75d619bd52bca9bbf9f861f226f97afc19e70413`  
		Last Modified: Fri, 22 Aug 2025 03:19:42 GMT  
		Size: 1.6 MB (1567069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddcc9f0e9b433e088c2545cbd386786132bc494afa98bbf9cceb57617d2d367`  
		Last Modified: Fri, 29 Aug 2025 14:11:28 GMT  
		Size: 161.0 MB (160963840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:bce66f6d4297b47739c0954c0afb8a0d7ce89f167c49c26bb1aeb3183b4178d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d2a55131dba91a6d7993453feca1bc13eb3c878c7a270118bccf37a300adc0`

```dockerfile
```

-	Layers:
	-	`sha256:0082cc5e010b406fa5e9b523d55c695237a6177c1d766f114194870d8bf70c8e`  
		Last Modified: Fri, 29 Aug 2025 14:53:23 GMT  
		Size: 20.7 KB (20733 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.0-162.1.beta`

```console
$ docker pull dart@sha256:c680b27a454907cd60ff97e39eece9d0325bbe31d3f5161149751528c06ac8af
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

### `dart:3.10.0-162.1.beta` - linux; amd64

```console
$ docker pull dart@sha256:1a46b3b3f620c5d5768e39d69eb62bcbb7f6d13f008afe867e9fa5690d24f9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285670197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de20559c49c5a67c500caac405bfd819bb813a9d08264407fbe0d3e96b0e25e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Sep 2025 11:42:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf9fed122ce01d0d526ae8692f928dd716d18a204d4cf0c3f0738172c3e7c5b`  
		Last Modified: Mon, 08 Sep 2025 23:53:57 GMT  
		Size: 42.5 MB (42482620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8d2919d332a6dfc0a0951be7d09b78225add11c58b19a0704dc4b05fbb04fb`  
		Last Modified: Mon, 08 Sep 2025 21:42:43 GMT  
		Size: 1.9 MB (1873613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5355f8e74c7f5d3ba881899b79bccd28fc0b15dc55dd3ade9306ea4ab78cd523`  
		Last Modified: Mon, 08 Sep 2025 23:55:12 GMT  
		Size: 211.5 MB (211540437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-162.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:3690c2fa464a0e0a6d3d5c679d18bd99f76efd43a71b46925135560642038f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5189abae3c1fbe669d632e7274f9b35b9ca90c52880bad7ce3ca8f73277f281d`

```dockerfile
```

-	Layers:
	-	`sha256:b38c5b011136b0e5cfcafeee9f1b6ea2af118f10e0258f14e5cee5af8ad84c43`  
		Last Modified: Mon, 08 Sep 2025 23:53:36 GMT  
		Size: 19.0 KB (18966 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-162.1.beta` - linux; arm variant v7

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

### `dart:3.10.0-162.1.beta` - unknown; unknown

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

### `dart:3.10.0-162.1.beta` - linux; arm64 variant v8

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

### `dart:3.10.0-162.1.beta` - unknown; unknown

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

### `dart:3.10.0-162.1.beta` - linux; riscv64

```console
$ docker pull dart@sha256:8c5d9e01c9a920d890dec85bb44f6348e7b763b4b7299ec0ab24542d1b3c7d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231816349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9595bfa9ee5316262c4d6ef6abca4012e1d0c5a1d95055dcc5d9dc7a1f83a5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
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
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a205fca315a844d9ccc027e5e049ad2e65faf49acb3ecd44fc33c8f28940b369`  
		Last Modified: Fri, 05 Sep 2025 13:24:28 GMT  
		Size: 41.5 MB (41549880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc41e3eb052c31c511c6a34ed71719ea35f7be91f2e01a723f0ec1b019d75e3`  
		Last Modified: Fri, 05 Sep 2025 13:24:02 GMT  
		Size: 1.6 MB (1567068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0452708e5f4970931790acb5a6ce7836c24dd18b3009f9a04e316bc762178f`  
		Last Modified: Fri, 05 Sep 2025 14:52:55 GMT  
		Size: 160.4 MB (160427746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-162.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:88e2afd0ca5d2dbf9aff31a2357cf7b26f7c62f9d822f3f5173fb90453a1e363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba5cf20dedf29a5023834ffa6993599ac485f7edd0456b320b8cf520be49b84`

```dockerfile
```

-	Layers:
	-	`sha256:1dd72b600575fb19b59e78cace1cbfddd7d0b0eb669c1a16c58ccd36139bc936`  
		Last Modified: Fri, 05 Sep 2025 14:53:25 GMT  
		Size: 19.0 KB (19014 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.0-162.1.beta-sdk`

```console
$ docker pull dart@sha256:c680b27a454907cd60ff97e39eece9d0325bbe31d3f5161149751528c06ac8af
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

### `dart:3.10.0-162.1.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:1a46b3b3f620c5d5768e39d69eb62bcbb7f6d13f008afe867e9fa5690d24f9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285670197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de20559c49c5a67c500caac405bfd819bb813a9d08264407fbe0d3e96b0e25e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Sep 2025 11:42:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf9fed122ce01d0d526ae8692f928dd716d18a204d4cf0c3f0738172c3e7c5b`  
		Last Modified: Mon, 08 Sep 2025 23:53:57 GMT  
		Size: 42.5 MB (42482620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8d2919d332a6dfc0a0951be7d09b78225add11c58b19a0704dc4b05fbb04fb`  
		Last Modified: Mon, 08 Sep 2025 21:42:43 GMT  
		Size: 1.9 MB (1873613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5355f8e74c7f5d3ba881899b79bccd28fc0b15dc55dd3ade9306ea4ab78cd523`  
		Last Modified: Mon, 08 Sep 2025 23:55:12 GMT  
		Size: 211.5 MB (211540437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-162.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:3690c2fa464a0e0a6d3d5c679d18bd99f76efd43a71b46925135560642038f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5189abae3c1fbe669d632e7274f9b35b9ca90c52880bad7ce3ca8f73277f281d`

```dockerfile
```

-	Layers:
	-	`sha256:b38c5b011136b0e5cfcafeee9f1b6ea2af118f10e0258f14e5cee5af8ad84c43`  
		Last Modified: Mon, 08 Sep 2025 23:53:36 GMT  
		Size: 19.0 KB (18966 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-162.1.beta-sdk` - linux; arm variant v7

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

### `dart:3.10.0-162.1.beta-sdk` - unknown; unknown

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

### `dart:3.10.0-162.1.beta-sdk` - linux; arm64 variant v8

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

### `dart:3.10.0-162.1.beta-sdk` - unknown; unknown

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

### `dart:3.10.0-162.1.beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:8c5d9e01c9a920d890dec85bb44f6348e7b763b4b7299ec0ab24542d1b3c7d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231816349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9595bfa9ee5316262c4d6ef6abca4012e1d0c5a1d95055dcc5d9dc7a1f83a5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
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
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a205fca315a844d9ccc027e5e049ad2e65faf49acb3ecd44fc33c8f28940b369`  
		Last Modified: Fri, 05 Sep 2025 13:24:28 GMT  
		Size: 41.5 MB (41549880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc41e3eb052c31c511c6a34ed71719ea35f7be91f2e01a723f0ec1b019d75e3`  
		Last Modified: Fri, 05 Sep 2025 13:24:02 GMT  
		Size: 1.6 MB (1567068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0452708e5f4970931790acb5a6ce7836c24dd18b3009f9a04e316bc762178f`  
		Last Modified: Fri, 05 Sep 2025 14:52:55 GMT  
		Size: 160.4 MB (160427746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-162.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:88e2afd0ca5d2dbf9aff31a2357cf7b26f7c62f9d822f3f5173fb90453a1e363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba5cf20dedf29a5023834ffa6993599ac485f7edd0456b320b8cf520be49b84`

```dockerfile
```

-	Layers:
	-	`sha256:1dd72b600575fb19b59e78cace1cbfddd7d0b0eb669c1a16c58ccd36139bc936`  
		Last Modified: Fri, 05 Sep 2025 14:53:25 GMT  
		Size: 19.0 KB (19014 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9`

```console
$ docker pull dart@sha256:cc4d50f840b502dde7068fca505efedad0802817b15b78218b4512396717464a
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
$ docker pull dart@sha256:3e66cf04d5ede710f73734d83c49fe5f598729f668c4405e182642be071633d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295375890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d74785f94badad3736afeb4f7b76e9d43b4857aaafa417cea6b388f06959e30`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Sep 2025 11:42:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05c4aceb529f35f93eb6f1738babefcc3b2a7b2711d60e096f1460aa9f7dbae`  
		Last Modified: Mon, 08 Sep 2025 22:09:12 GMT  
		Size: 42.5 MB (42482593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677702b67ee1965df50e8ff7bab9200d6d743530e36e1b42449bbd70797ed751`  
		Last Modified: Mon, 08 Sep 2025 21:42:42 GMT  
		Size: 1.9 MB (1873612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e8b7557068bfac0eba4dd938e4106f62ce53b7dfe00f994ef29ee540375007`  
		Last Modified: Mon, 08 Sep 2025 22:09:11 GMT  
		Size: 221.2 MB (221246158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:57c77b466c4fdbc8b68d3e27de68f3c1ed005a8578d1337ccb4f79aaf16fc06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494a0f550d210d3f67be8f09d39f230732d45f2693dbb952b6da288add8c5f26`

```dockerfile
```

-	Layers:
	-	`sha256:e35e641e01735e6bbe594b05c7c452e632dd7974107ee3a3e6077d78a6f89af9`  
		Last Modified: Mon, 08 Sep 2025 23:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9` - linux; arm variant v7

```console
$ docker pull dart@sha256:34051496922f2a4ede768b1340880bdb586c93b08880e93fa0a9202efd6a385d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220750428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f328cd29cfc7c7bdbebb76a23f626c68f4dacf31e7ad16d3e00dad21f5437e`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56836f0c8e8c91ed8d9b18dcd856474127d1246651d41c7a7e1d85c5aa587e7`  
		Last Modified: Mon, 08 Sep 2025 23:12:50 GMT  
		Size: 37.5 MB (37478354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55445b8ad1d9275c46905f2852157c3dea0ba0d8318f4165761fdbc4a4d1804f`  
		Last Modified: Mon, 08 Sep 2025 22:47:12 GMT  
		Size: 1.3 MB (1275112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836ea90eeff7caed8d596d2ebd8d662040dac66c7d25e191612897e12c08911d`  
		Last Modified: Mon, 08 Sep 2025 23:12:42 GMT  
		Size: 155.8 MB (155789083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:0df9580b782efa5922674f248545627fa84db083825a4e488475bc2c245b2a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391e8aae71d36fc2f2abf20bf2fff2f507db492df051c3d7b57117589ed3c492`

```dockerfile
```

-	Layers:
	-	`sha256:061e9d6d0f6c9b75254d85de65985c3e07a743a84cda822a5ffb31980d39df13`  
		Last Modified: Mon, 08 Sep 2025 23:53:26 GMT  
		Size: 20.8 KB (20804 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:a97c783bb9e61ae8e7c7f8038e236fc6150abe9eca36ff0edaee0aee8b70920c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294659560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b214cc2238e49e232fecafca40cee02d5cfb266fc3faf3db364061d70b51e31`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c190eda88054318fcbdee78d8ef8cae137f19117a7e2bec8cc689ce5b64343`  
		Last Modified: Mon, 08 Sep 2025 23:53:48 GMT  
		Size: 42.3 MB (42270213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29205cde420f3386a6ec932407c0e575887fc341ae65db74ea280da3c6623f5`  
		Last Modified: Mon, 08 Sep 2025 22:25:11 GMT  
		Size: 1.6 MB (1566648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b121f20624a7437e0ea7c95f071379390a425cf722473abab14cd23cb34732`  
		Last Modified: Mon, 08 Sep 2025 23:53:51 GMT  
		Size: 220.7 MB (220686036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:297f008f6b5a02b796303bcff9642a65fd7849749ea887ccf39e3d8addc47ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c61a8b35b2aa67809ba8bdcc5eb7a48c23ea623044e44a13278599ea4374ee`

```dockerfile
```

-	Layers:
	-	`sha256:9a072058476f89d2d11b4b1e8f47b1501e0c353ae192e8928ecff1a605717089`  
		Last Modified: Mon, 08 Sep 2025 23:53:29 GMT  
		Size: 20.9 KB (20855 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9` - linux; riscv64

```console
$ docker pull dart@sha256:a23a20664bad82073426026d01cd12f3f78729248a9a2b7fb3a1c3d7cfb709d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232352464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db3501795667e769c99accfe9399dd1d60358614edcd0644c96f5b1f122a121`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 27 Aug 2025 13:56:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 27 Aug 2025 13:56:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Aug 2025 13:56:45 GMT
WORKDIR /root
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f4927a3b04f70ec84088797f16339585618b2ec5aa5be4346e1db849de61a9`  
		Last Modified: Fri, 22 Aug 2025 03:19:46 GMT  
		Size: 41.5 MB (41549900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c103a39452af771458a8486e75d619bd52bca9bbf9f861f226f97afc19e70413`  
		Last Modified: Fri, 22 Aug 2025 03:19:42 GMT  
		Size: 1.6 MB (1567069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddcc9f0e9b433e088c2545cbd386786132bc494afa98bbf9cceb57617d2d367`  
		Last Modified: Fri, 29 Aug 2025 14:11:28 GMT  
		Size: 161.0 MB (160963840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:bce66f6d4297b47739c0954c0afb8a0d7ce89f167c49c26bb1aeb3183b4178d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d2a55131dba91a6d7993453feca1bc13eb3c878c7a270118bccf37a300adc0`

```dockerfile
```

-	Layers:
	-	`sha256:0082cc5e010b406fa5e9b523d55c695237a6177c1d766f114194870d8bf70c8e`  
		Last Modified: Fri, 29 Aug 2025 14:53:23 GMT  
		Size: 20.7 KB (20733 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9-sdk`

```console
$ docker pull dart@sha256:cc4d50f840b502dde7068fca505efedad0802817b15b78218b4512396717464a
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
$ docker pull dart@sha256:3e66cf04d5ede710f73734d83c49fe5f598729f668c4405e182642be071633d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295375890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d74785f94badad3736afeb4f7b76e9d43b4857aaafa417cea6b388f06959e30`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Sep 2025 11:42:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05c4aceb529f35f93eb6f1738babefcc3b2a7b2711d60e096f1460aa9f7dbae`  
		Last Modified: Mon, 08 Sep 2025 22:09:12 GMT  
		Size: 42.5 MB (42482593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677702b67ee1965df50e8ff7bab9200d6d743530e36e1b42449bbd70797ed751`  
		Last Modified: Mon, 08 Sep 2025 21:42:42 GMT  
		Size: 1.9 MB (1873612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e8b7557068bfac0eba4dd938e4106f62ce53b7dfe00f994ef29ee540375007`  
		Last Modified: Mon, 08 Sep 2025 22:09:11 GMT  
		Size: 221.2 MB (221246158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:57c77b466c4fdbc8b68d3e27de68f3c1ed005a8578d1337ccb4f79aaf16fc06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494a0f550d210d3f67be8f09d39f230732d45f2693dbb952b6da288add8c5f26`

```dockerfile
```

-	Layers:
	-	`sha256:e35e641e01735e6bbe594b05c7c452e632dd7974107ee3a3e6077d78a6f89af9`  
		Last Modified: Mon, 08 Sep 2025 23:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:34051496922f2a4ede768b1340880bdb586c93b08880e93fa0a9202efd6a385d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220750428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f328cd29cfc7c7bdbebb76a23f626c68f4dacf31e7ad16d3e00dad21f5437e`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56836f0c8e8c91ed8d9b18dcd856474127d1246651d41c7a7e1d85c5aa587e7`  
		Last Modified: Mon, 08 Sep 2025 23:12:50 GMT  
		Size: 37.5 MB (37478354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55445b8ad1d9275c46905f2852157c3dea0ba0d8318f4165761fdbc4a4d1804f`  
		Last Modified: Mon, 08 Sep 2025 22:47:12 GMT  
		Size: 1.3 MB (1275112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836ea90eeff7caed8d596d2ebd8d662040dac66c7d25e191612897e12c08911d`  
		Last Modified: Mon, 08 Sep 2025 23:12:42 GMT  
		Size: 155.8 MB (155789083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0df9580b782efa5922674f248545627fa84db083825a4e488475bc2c245b2a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391e8aae71d36fc2f2abf20bf2fff2f507db492df051c3d7b57117589ed3c492`

```dockerfile
```

-	Layers:
	-	`sha256:061e9d6d0f6c9b75254d85de65985c3e07a743a84cda822a5ffb31980d39df13`  
		Last Modified: Mon, 08 Sep 2025 23:53:26 GMT  
		Size: 20.8 KB (20804 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:a97c783bb9e61ae8e7c7f8038e236fc6150abe9eca36ff0edaee0aee8b70920c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294659560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b214cc2238e49e232fecafca40cee02d5cfb266fc3faf3db364061d70b51e31`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c190eda88054318fcbdee78d8ef8cae137f19117a7e2bec8cc689ce5b64343`  
		Last Modified: Mon, 08 Sep 2025 23:53:48 GMT  
		Size: 42.3 MB (42270213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29205cde420f3386a6ec932407c0e575887fc341ae65db74ea280da3c6623f5`  
		Last Modified: Mon, 08 Sep 2025 22:25:11 GMT  
		Size: 1.6 MB (1566648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b121f20624a7437e0ea7c95f071379390a425cf722473abab14cd23cb34732`  
		Last Modified: Mon, 08 Sep 2025 23:53:51 GMT  
		Size: 220.7 MB (220686036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:297f008f6b5a02b796303bcff9642a65fd7849749ea887ccf39e3d8addc47ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c61a8b35b2aa67809ba8bdcc5eb7a48c23ea623044e44a13278599ea4374ee`

```dockerfile
```

-	Layers:
	-	`sha256:9a072058476f89d2d11b4b1e8f47b1501e0c353ae192e8928ecff1a605717089`  
		Last Modified: Mon, 08 Sep 2025 23:53:29 GMT  
		Size: 20.9 KB (20855 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:a23a20664bad82073426026d01cd12f3f78729248a9a2b7fb3a1c3d7cfb709d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232352464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db3501795667e769c99accfe9399dd1d60358614edcd0644c96f5b1f122a121`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 27 Aug 2025 13:56:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 27 Aug 2025 13:56:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Aug 2025 13:56:45 GMT
WORKDIR /root
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f4927a3b04f70ec84088797f16339585618b2ec5aa5be4346e1db849de61a9`  
		Last Modified: Fri, 22 Aug 2025 03:19:46 GMT  
		Size: 41.5 MB (41549900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c103a39452af771458a8486e75d619bd52bca9bbf9f861f226f97afc19e70413`  
		Last Modified: Fri, 22 Aug 2025 03:19:42 GMT  
		Size: 1.6 MB (1567069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddcc9f0e9b433e088c2545cbd386786132bc494afa98bbf9cceb57617d2d367`  
		Last Modified: Fri, 29 Aug 2025 14:11:28 GMT  
		Size: 161.0 MB (160963840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:bce66f6d4297b47739c0954c0afb8a0d7ce89f167c49c26bb1aeb3183b4178d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d2a55131dba91a6d7993453feca1bc13eb3c878c7a270118bccf37a300adc0`

```dockerfile
```

-	Layers:
	-	`sha256:0082cc5e010b406fa5e9b523d55c695237a6177c1d766f114194870d8bf70c8e`  
		Last Modified: Fri, 29 Aug 2025 14:53:23 GMT  
		Size: 20.7 KB (20733 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9.2`

```console
$ docker pull dart@sha256:cc4d50f840b502dde7068fca505efedad0802817b15b78218b4512396717464a
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

### `dart:3.9.2` - linux; amd64

```console
$ docker pull dart@sha256:3e66cf04d5ede710f73734d83c49fe5f598729f668c4405e182642be071633d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295375890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d74785f94badad3736afeb4f7b76e9d43b4857aaafa417cea6b388f06959e30`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Sep 2025 11:42:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05c4aceb529f35f93eb6f1738babefcc3b2a7b2711d60e096f1460aa9f7dbae`  
		Last Modified: Mon, 08 Sep 2025 22:09:12 GMT  
		Size: 42.5 MB (42482593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677702b67ee1965df50e8ff7bab9200d6d743530e36e1b42449bbd70797ed751`  
		Last Modified: Mon, 08 Sep 2025 21:42:42 GMT  
		Size: 1.9 MB (1873612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e8b7557068bfac0eba4dd938e4106f62ce53b7dfe00f994ef29ee540375007`  
		Last Modified: Mon, 08 Sep 2025 22:09:11 GMT  
		Size: 221.2 MB (221246158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.2` - unknown; unknown

```console
$ docker pull dart@sha256:57c77b466c4fdbc8b68d3e27de68f3c1ed005a8578d1337ccb4f79aaf16fc06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494a0f550d210d3f67be8f09d39f230732d45f2693dbb952b6da288add8c5f26`

```dockerfile
```

-	Layers:
	-	`sha256:e35e641e01735e6bbe594b05c7c452e632dd7974107ee3a3e6077d78a6f89af9`  
		Last Modified: Mon, 08 Sep 2025 23:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.2` - linux; arm variant v7

```console
$ docker pull dart@sha256:34051496922f2a4ede768b1340880bdb586c93b08880e93fa0a9202efd6a385d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220750428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f328cd29cfc7c7bdbebb76a23f626c68f4dacf31e7ad16d3e00dad21f5437e`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56836f0c8e8c91ed8d9b18dcd856474127d1246651d41c7a7e1d85c5aa587e7`  
		Last Modified: Mon, 08 Sep 2025 23:12:50 GMT  
		Size: 37.5 MB (37478354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55445b8ad1d9275c46905f2852157c3dea0ba0d8318f4165761fdbc4a4d1804f`  
		Last Modified: Mon, 08 Sep 2025 22:47:12 GMT  
		Size: 1.3 MB (1275112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836ea90eeff7caed8d596d2ebd8d662040dac66c7d25e191612897e12c08911d`  
		Last Modified: Mon, 08 Sep 2025 23:12:42 GMT  
		Size: 155.8 MB (155789083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.2` - unknown; unknown

```console
$ docker pull dart@sha256:0df9580b782efa5922674f248545627fa84db083825a4e488475bc2c245b2a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391e8aae71d36fc2f2abf20bf2fff2f507db492df051c3d7b57117589ed3c492`

```dockerfile
```

-	Layers:
	-	`sha256:061e9d6d0f6c9b75254d85de65985c3e07a743a84cda822a5ffb31980d39df13`  
		Last Modified: Mon, 08 Sep 2025 23:53:26 GMT  
		Size: 20.8 KB (20804 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.2` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:a97c783bb9e61ae8e7c7f8038e236fc6150abe9eca36ff0edaee0aee8b70920c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294659560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b214cc2238e49e232fecafca40cee02d5cfb266fc3faf3db364061d70b51e31`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c190eda88054318fcbdee78d8ef8cae137f19117a7e2bec8cc689ce5b64343`  
		Last Modified: Mon, 08 Sep 2025 23:53:48 GMT  
		Size: 42.3 MB (42270213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29205cde420f3386a6ec932407c0e575887fc341ae65db74ea280da3c6623f5`  
		Last Modified: Mon, 08 Sep 2025 22:25:11 GMT  
		Size: 1.6 MB (1566648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b121f20624a7437e0ea7c95f071379390a425cf722473abab14cd23cb34732`  
		Last Modified: Mon, 08 Sep 2025 23:53:51 GMT  
		Size: 220.7 MB (220686036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.2` - unknown; unknown

```console
$ docker pull dart@sha256:297f008f6b5a02b796303bcff9642a65fd7849749ea887ccf39e3d8addc47ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c61a8b35b2aa67809ba8bdcc5eb7a48c23ea623044e44a13278599ea4374ee`

```dockerfile
```

-	Layers:
	-	`sha256:9a072058476f89d2d11b4b1e8f47b1501e0c353ae192e8928ecff1a605717089`  
		Last Modified: Mon, 08 Sep 2025 23:53:29 GMT  
		Size: 20.9 KB (20855 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.2` - linux; riscv64

```console
$ docker pull dart@sha256:a23a20664bad82073426026d01cd12f3f78729248a9a2b7fb3a1c3d7cfb709d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232352464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db3501795667e769c99accfe9399dd1d60358614edcd0644c96f5b1f122a121`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 27 Aug 2025 13:56:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 27 Aug 2025 13:56:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Aug 2025 13:56:45 GMT
WORKDIR /root
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f4927a3b04f70ec84088797f16339585618b2ec5aa5be4346e1db849de61a9`  
		Last Modified: Fri, 22 Aug 2025 03:19:46 GMT  
		Size: 41.5 MB (41549900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c103a39452af771458a8486e75d619bd52bca9bbf9f861f226f97afc19e70413`  
		Last Modified: Fri, 22 Aug 2025 03:19:42 GMT  
		Size: 1.6 MB (1567069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddcc9f0e9b433e088c2545cbd386786132bc494afa98bbf9cceb57617d2d367`  
		Last Modified: Fri, 29 Aug 2025 14:11:28 GMT  
		Size: 161.0 MB (160963840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.2` - unknown; unknown

```console
$ docker pull dart@sha256:bce66f6d4297b47739c0954c0afb8a0d7ce89f167c49c26bb1aeb3183b4178d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d2a55131dba91a6d7993453feca1bc13eb3c878c7a270118bccf37a300adc0`

```dockerfile
```

-	Layers:
	-	`sha256:0082cc5e010b406fa5e9b523d55c695237a6177c1d766f114194870d8bf70c8e`  
		Last Modified: Fri, 29 Aug 2025 14:53:23 GMT  
		Size: 20.7 KB (20733 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9.2-sdk`

```console
$ docker pull dart@sha256:cc4d50f840b502dde7068fca505efedad0802817b15b78218b4512396717464a
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

### `dart:3.9.2-sdk` - linux; amd64

```console
$ docker pull dart@sha256:3e66cf04d5ede710f73734d83c49fe5f598729f668c4405e182642be071633d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295375890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d74785f94badad3736afeb4f7b76e9d43b4857aaafa417cea6b388f06959e30`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Sep 2025 11:42:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05c4aceb529f35f93eb6f1738babefcc3b2a7b2711d60e096f1460aa9f7dbae`  
		Last Modified: Mon, 08 Sep 2025 22:09:12 GMT  
		Size: 42.5 MB (42482593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677702b67ee1965df50e8ff7bab9200d6d743530e36e1b42449bbd70797ed751`  
		Last Modified: Mon, 08 Sep 2025 21:42:42 GMT  
		Size: 1.9 MB (1873612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e8b7557068bfac0eba4dd938e4106f62ce53b7dfe00f994ef29ee540375007`  
		Last Modified: Mon, 08 Sep 2025 22:09:11 GMT  
		Size: 221.2 MB (221246158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.2-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:57c77b466c4fdbc8b68d3e27de68f3c1ed005a8578d1337ccb4f79aaf16fc06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494a0f550d210d3f67be8f09d39f230732d45f2693dbb952b6da288add8c5f26`

```dockerfile
```

-	Layers:
	-	`sha256:e35e641e01735e6bbe594b05c7c452e632dd7974107ee3a3e6077d78a6f89af9`  
		Last Modified: Mon, 08 Sep 2025 23:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.2-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:34051496922f2a4ede768b1340880bdb586c93b08880e93fa0a9202efd6a385d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220750428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f328cd29cfc7c7bdbebb76a23f626c68f4dacf31e7ad16d3e00dad21f5437e`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56836f0c8e8c91ed8d9b18dcd856474127d1246651d41c7a7e1d85c5aa587e7`  
		Last Modified: Mon, 08 Sep 2025 23:12:50 GMT  
		Size: 37.5 MB (37478354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55445b8ad1d9275c46905f2852157c3dea0ba0d8318f4165761fdbc4a4d1804f`  
		Last Modified: Mon, 08 Sep 2025 22:47:12 GMT  
		Size: 1.3 MB (1275112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836ea90eeff7caed8d596d2ebd8d662040dac66c7d25e191612897e12c08911d`  
		Last Modified: Mon, 08 Sep 2025 23:12:42 GMT  
		Size: 155.8 MB (155789083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.2-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0df9580b782efa5922674f248545627fa84db083825a4e488475bc2c245b2a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391e8aae71d36fc2f2abf20bf2fff2f507db492df051c3d7b57117589ed3c492`

```dockerfile
```

-	Layers:
	-	`sha256:061e9d6d0f6c9b75254d85de65985c3e07a743a84cda822a5ffb31980d39df13`  
		Last Modified: Mon, 08 Sep 2025 23:53:26 GMT  
		Size: 20.8 KB (20804 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.2-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:a97c783bb9e61ae8e7c7f8038e236fc6150abe9eca36ff0edaee0aee8b70920c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294659560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b214cc2238e49e232fecafca40cee02d5cfb266fc3faf3db364061d70b51e31`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c190eda88054318fcbdee78d8ef8cae137f19117a7e2bec8cc689ce5b64343`  
		Last Modified: Mon, 08 Sep 2025 23:53:48 GMT  
		Size: 42.3 MB (42270213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29205cde420f3386a6ec932407c0e575887fc341ae65db74ea280da3c6623f5`  
		Last Modified: Mon, 08 Sep 2025 22:25:11 GMT  
		Size: 1.6 MB (1566648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b121f20624a7437e0ea7c95f071379390a425cf722473abab14cd23cb34732`  
		Last Modified: Mon, 08 Sep 2025 23:53:51 GMT  
		Size: 220.7 MB (220686036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.2-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:297f008f6b5a02b796303bcff9642a65fd7849749ea887ccf39e3d8addc47ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c61a8b35b2aa67809ba8bdcc5eb7a48c23ea623044e44a13278599ea4374ee`

```dockerfile
```

-	Layers:
	-	`sha256:9a072058476f89d2d11b4b1e8f47b1501e0c353ae192e8928ecff1a605717089`  
		Last Modified: Mon, 08 Sep 2025 23:53:29 GMT  
		Size: 20.9 KB (20855 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.2-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:a23a20664bad82073426026d01cd12f3f78729248a9a2b7fb3a1c3d7cfb709d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232352464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db3501795667e769c99accfe9399dd1d60358614edcd0644c96f5b1f122a121`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 27 Aug 2025 13:56:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 27 Aug 2025 13:56:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Aug 2025 13:56:45 GMT
WORKDIR /root
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f4927a3b04f70ec84088797f16339585618b2ec5aa5be4346e1db849de61a9`  
		Last Modified: Fri, 22 Aug 2025 03:19:46 GMT  
		Size: 41.5 MB (41549900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c103a39452af771458a8486e75d619bd52bca9bbf9f861f226f97afc19e70413`  
		Last Modified: Fri, 22 Aug 2025 03:19:42 GMT  
		Size: 1.6 MB (1567069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddcc9f0e9b433e088c2545cbd386786132bc494afa98bbf9cceb57617d2d367`  
		Last Modified: Fri, 29 Aug 2025 14:11:28 GMT  
		Size: 161.0 MB (160963840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.2-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:bce66f6d4297b47739c0954c0afb8a0d7ce89f167c49c26bb1aeb3183b4178d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d2a55131dba91a6d7993453feca1bc13eb3c878c7a270118bccf37a300adc0`

```dockerfile
```

-	Layers:
	-	`sha256:0082cc5e010b406fa5e9b523d55c695237a6177c1d766f114194870d8bf70c8e`  
		Last Modified: Fri, 29 Aug 2025 14:53:23 GMT  
		Size: 20.7 KB (20733 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:c680b27a454907cd60ff97e39eece9d0325bbe31d3f5161149751528c06ac8af
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
$ docker pull dart@sha256:1a46b3b3f620c5d5768e39d69eb62bcbb7f6d13f008afe867e9fa5690d24f9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285670197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de20559c49c5a67c500caac405bfd819bb813a9d08264407fbe0d3e96b0e25e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Sep 2025 11:42:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf9fed122ce01d0d526ae8692f928dd716d18a204d4cf0c3f0738172c3e7c5b`  
		Last Modified: Mon, 08 Sep 2025 23:53:57 GMT  
		Size: 42.5 MB (42482620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8d2919d332a6dfc0a0951be7d09b78225add11c58b19a0704dc4b05fbb04fb`  
		Last Modified: Mon, 08 Sep 2025 21:42:43 GMT  
		Size: 1.9 MB (1873613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5355f8e74c7f5d3ba881899b79bccd28fc0b15dc55dd3ade9306ea4ab78cd523`  
		Last Modified: Mon, 08 Sep 2025 23:55:12 GMT  
		Size: 211.5 MB (211540437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:3690c2fa464a0e0a6d3d5c679d18bd99f76efd43a71b46925135560642038f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5189abae3c1fbe669d632e7274f9b35b9ca90c52880bad7ce3ca8f73277f281d`

```dockerfile
```

-	Layers:
	-	`sha256:b38c5b011136b0e5cfcafeee9f1b6ea2af118f10e0258f14e5cee5af8ad84c43`  
		Last Modified: Mon, 08 Sep 2025 23:53:36 GMT  
		Size: 19.0 KB (18966 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

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

### `dart:beta` - unknown; unknown

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

### `dart:beta` - linux; arm64 variant v8

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

### `dart:beta` - unknown; unknown

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

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:8c5d9e01c9a920d890dec85bb44f6348e7b763b4b7299ec0ab24542d1b3c7d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231816349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9595bfa9ee5316262c4d6ef6abca4012e1d0c5a1d95055dcc5d9dc7a1f83a5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
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
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a205fca315a844d9ccc027e5e049ad2e65faf49acb3ecd44fc33c8f28940b369`  
		Last Modified: Fri, 05 Sep 2025 13:24:28 GMT  
		Size: 41.5 MB (41549880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc41e3eb052c31c511c6a34ed71719ea35f7be91f2e01a723f0ec1b019d75e3`  
		Last Modified: Fri, 05 Sep 2025 13:24:02 GMT  
		Size: 1.6 MB (1567068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0452708e5f4970931790acb5a6ce7836c24dd18b3009f9a04e316bc762178f`  
		Last Modified: Fri, 05 Sep 2025 14:52:55 GMT  
		Size: 160.4 MB (160427746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:88e2afd0ca5d2dbf9aff31a2357cf7b26f7c62f9d822f3f5173fb90453a1e363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba5cf20dedf29a5023834ffa6993599ac485f7edd0456b320b8cf520be49b84`

```dockerfile
```

-	Layers:
	-	`sha256:1dd72b600575fb19b59e78cace1cbfddd7d0b0eb669c1a16c58ccd36139bc936`  
		Last Modified: Fri, 05 Sep 2025 14:53:25 GMT  
		Size: 19.0 KB (19014 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:c680b27a454907cd60ff97e39eece9d0325bbe31d3f5161149751528c06ac8af
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
$ docker pull dart@sha256:1a46b3b3f620c5d5768e39d69eb62bcbb7f6d13f008afe867e9fa5690d24f9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285670197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de20559c49c5a67c500caac405bfd819bb813a9d08264407fbe0d3e96b0e25e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Sep 2025 11:42:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf9fed122ce01d0d526ae8692f928dd716d18a204d4cf0c3f0738172c3e7c5b`  
		Last Modified: Mon, 08 Sep 2025 23:53:57 GMT  
		Size: 42.5 MB (42482620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8d2919d332a6dfc0a0951be7d09b78225add11c58b19a0704dc4b05fbb04fb`  
		Last Modified: Mon, 08 Sep 2025 21:42:43 GMT  
		Size: 1.9 MB (1873613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5355f8e74c7f5d3ba881899b79bccd28fc0b15dc55dd3ade9306ea4ab78cd523`  
		Last Modified: Mon, 08 Sep 2025 23:55:12 GMT  
		Size: 211.5 MB (211540437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:3690c2fa464a0e0a6d3d5c679d18bd99f76efd43a71b46925135560642038f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5189abae3c1fbe669d632e7274f9b35b9ca90c52880bad7ce3ca8f73277f281d`

```dockerfile
```

-	Layers:
	-	`sha256:b38c5b011136b0e5cfcafeee9f1b6ea2af118f10e0258f14e5cee5af8ad84c43`  
		Last Modified: Mon, 08 Sep 2025 23:53:36 GMT  
		Size: 19.0 KB (18966 bytes)  
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
$ docker pull dart@sha256:8c5d9e01c9a920d890dec85bb44f6348e7b763b4b7299ec0ab24542d1b3c7d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231816349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9595bfa9ee5316262c4d6ef6abca4012e1d0c5a1d95055dcc5d9dc7a1f83a5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
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
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a205fca315a844d9ccc027e5e049ad2e65faf49acb3ecd44fc33c8f28940b369`  
		Last Modified: Fri, 05 Sep 2025 13:24:28 GMT  
		Size: 41.5 MB (41549880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc41e3eb052c31c511c6a34ed71719ea35f7be91f2e01a723f0ec1b019d75e3`  
		Last Modified: Fri, 05 Sep 2025 13:24:02 GMT  
		Size: 1.6 MB (1567068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0452708e5f4970931790acb5a6ce7836c24dd18b3009f9a04e316bc762178f`  
		Last Modified: Fri, 05 Sep 2025 14:52:55 GMT  
		Size: 160.4 MB (160427746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:88e2afd0ca5d2dbf9aff31a2357cf7b26f7c62f9d822f3f5173fb90453a1e363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba5cf20dedf29a5023834ffa6993599ac485f7edd0456b320b8cf520be49b84`

```dockerfile
```

-	Layers:
	-	`sha256:1dd72b600575fb19b59e78cace1cbfddd7d0b0eb669c1a16c58ccd36139bc936`  
		Last Modified: Fri, 05 Sep 2025 14:53:25 GMT  
		Size: 19.0 KB (19014 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:cc4d50f840b502dde7068fca505efedad0802817b15b78218b4512396717464a
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
$ docker pull dart@sha256:3e66cf04d5ede710f73734d83c49fe5f598729f668c4405e182642be071633d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295375890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d74785f94badad3736afeb4f7b76e9d43b4857aaafa417cea6b388f06959e30`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Sep 2025 11:42:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05c4aceb529f35f93eb6f1738babefcc3b2a7b2711d60e096f1460aa9f7dbae`  
		Last Modified: Mon, 08 Sep 2025 22:09:12 GMT  
		Size: 42.5 MB (42482593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677702b67ee1965df50e8ff7bab9200d6d743530e36e1b42449bbd70797ed751`  
		Last Modified: Mon, 08 Sep 2025 21:42:42 GMT  
		Size: 1.9 MB (1873612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e8b7557068bfac0eba4dd938e4106f62ce53b7dfe00f994ef29ee540375007`  
		Last Modified: Mon, 08 Sep 2025 22:09:11 GMT  
		Size: 221.2 MB (221246158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:57c77b466c4fdbc8b68d3e27de68f3c1ed005a8578d1337ccb4f79aaf16fc06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494a0f550d210d3f67be8f09d39f230732d45f2693dbb952b6da288add8c5f26`

```dockerfile
```

-	Layers:
	-	`sha256:e35e641e01735e6bbe594b05c7c452e632dd7974107ee3a3e6077d78a6f89af9`  
		Last Modified: Mon, 08 Sep 2025 23:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:34051496922f2a4ede768b1340880bdb586c93b08880e93fa0a9202efd6a385d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220750428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f328cd29cfc7c7bdbebb76a23f626c68f4dacf31e7ad16d3e00dad21f5437e`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56836f0c8e8c91ed8d9b18dcd856474127d1246651d41c7a7e1d85c5aa587e7`  
		Last Modified: Mon, 08 Sep 2025 23:12:50 GMT  
		Size: 37.5 MB (37478354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55445b8ad1d9275c46905f2852157c3dea0ba0d8318f4165761fdbc4a4d1804f`  
		Last Modified: Mon, 08 Sep 2025 22:47:12 GMT  
		Size: 1.3 MB (1275112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836ea90eeff7caed8d596d2ebd8d662040dac66c7d25e191612897e12c08911d`  
		Last Modified: Mon, 08 Sep 2025 23:12:42 GMT  
		Size: 155.8 MB (155789083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:0df9580b782efa5922674f248545627fa84db083825a4e488475bc2c245b2a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391e8aae71d36fc2f2abf20bf2fff2f507db492df051c3d7b57117589ed3c492`

```dockerfile
```

-	Layers:
	-	`sha256:061e9d6d0f6c9b75254d85de65985c3e07a743a84cda822a5ffb31980d39df13`  
		Last Modified: Mon, 08 Sep 2025 23:53:26 GMT  
		Size: 20.8 KB (20804 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:a97c783bb9e61ae8e7c7f8038e236fc6150abe9eca36ff0edaee0aee8b70920c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294659560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b214cc2238e49e232fecafca40cee02d5cfb266fc3faf3db364061d70b51e31`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c190eda88054318fcbdee78d8ef8cae137f19117a7e2bec8cc689ce5b64343`  
		Last Modified: Mon, 08 Sep 2025 23:53:48 GMT  
		Size: 42.3 MB (42270213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29205cde420f3386a6ec932407c0e575887fc341ae65db74ea280da3c6623f5`  
		Last Modified: Mon, 08 Sep 2025 22:25:11 GMT  
		Size: 1.6 MB (1566648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b121f20624a7437e0ea7c95f071379390a425cf722473abab14cd23cb34732`  
		Last Modified: Mon, 08 Sep 2025 23:53:51 GMT  
		Size: 220.7 MB (220686036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:297f008f6b5a02b796303bcff9642a65fd7849749ea887ccf39e3d8addc47ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c61a8b35b2aa67809ba8bdcc5eb7a48c23ea623044e44a13278599ea4374ee`

```dockerfile
```

-	Layers:
	-	`sha256:9a072058476f89d2d11b4b1e8f47b1501e0c353ae192e8928ecff1a605717089`  
		Last Modified: Mon, 08 Sep 2025 23:53:29 GMT  
		Size: 20.9 KB (20855 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; riscv64

```console
$ docker pull dart@sha256:a23a20664bad82073426026d01cd12f3f78729248a9a2b7fb3a1c3d7cfb709d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232352464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db3501795667e769c99accfe9399dd1d60358614edcd0644c96f5b1f122a121`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 27 Aug 2025 13:56:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 27 Aug 2025 13:56:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Aug 2025 13:56:45 GMT
WORKDIR /root
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f4927a3b04f70ec84088797f16339585618b2ec5aa5be4346e1db849de61a9`  
		Last Modified: Fri, 22 Aug 2025 03:19:46 GMT  
		Size: 41.5 MB (41549900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c103a39452af771458a8486e75d619bd52bca9bbf9f861f226f97afc19e70413`  
		Last Modified: Fri, 22 Aug 2025 03:19:42 GMT  
		Size: 1.6 MB (1567069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddcc9f0e9b433e088c2545cbd386786132bc494afa98bbf9cceb57617d2d367`  
		Last Modified: Fri, 29 Aug 2025 14:11:28 GMT  
		Size: 161.0 MB (160963840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:bce66f6d4297b47739c0954c0afb8a0d7ce89f167c49c26bb1aeb3183b4178d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d2a55131dba91a6d7993453feca1bc13eb3c878c7a270118bccf37a300adc0`

```dockerfile
```

-	Layers:
	-	`sha256:0082cc5e010b406fa5e9b523d55c695237a6177c1d766f114194870d8bf70c8e`  
		Last Modified: Fri, 29 Aug 2025 14:53:23 GMT  
		Size: 20.7 KB (20733 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:cc4d50f840b502dde7068fca505efedad0802817b15b78218b4512396717464a
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
$ docker pull dart@sha256:3e66cf04d5ede710f73734d83c49fe5f598729f668c4405e182642be071633d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295375890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d74785f94badad3736afeb4f7b76e9d43b4857aaafa417cea6b388f06959e30`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Sep 2025 11:42:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05c4aceb529f35f93eb6f1738babefcc3b2a7b2711d60e096f1460aa9f7dbae`  
		Last Modified: Mon, 08 Sep 2025 22:09:12 GMT  
		Size: 42.5 MB (42482593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677702b67ee1965df50e8ff7bab9200d6d743530e36e1b42449bbd70797ed751`  
		Last Modified: Mon, 08 Sep 2025 21:42:42 GMT  
		Size: 1.9 MB (1873612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e8b7557068bfac0eba4dd938e4106f62ce53b7dfe00f994ef29ee540375007`  
		Last Modified: Mon, 08 Sep 2025 22:09:11 GMT  
		Size: 221.2 MB (221246158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:57c77b466c4fdbc8b68d3e27de68f3c1ed005a8578d1337ccb4f79aaf16fc06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494a0f550d210d3f67be8f09d39f230732d45f2693dbb952b6da288add8c5f26`

```dockerfile
```

-	Layers:
	-	`sha256:e35e641e01735e6bbe594b05c7c452e632dd7974107ee3a3e6077d78a6f89af9`  
		Last Modified: Mon, 08 Sep 2025 23:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:34051496922f2a4ede768b1340880bdb586c93b08880e93fa0a9202efd6a385d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220750428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f328cd29cfc7c7bdbebb76a23f626c68f4dacf31e7ad16d3e00dad21f5437e`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56836f0c8e8c91ed8d9b18dcd856474127d1246651d41c7a7e1d85c5aa587e7`  
		Last Modified: Mon, 08 Sep 2025 23:12:50 GMT  
		Size: 37.5 MB (37478354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55445b8ad1d9275c46905f2852157c3dea0ba0d8318f4165761fdbc4a4d1804f`  
		Last Modified: Mon, 08 Sep 2025 22:47:12 GMT  
		Size: 1.3 MB (1275112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836ea90eeff7caed8d596d2ebd8d662040dac66c7d25e191612897e12c08911d`  
		Last Modified: Mon, 08 Sep 2025 23:12:42 GMT  
		Size: 155.8 MB (155789083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0df9580b782efa5922674f248545627fa84db083825a4e488475bc2c245b2a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391e8aae71d36fc2f2abf20bf2fff2f507db492df051c3d7b57117589ed3c492`

```dockerfile
```

-	Layers:
	-	`sha256:061e9d6d0f6c9b75254d85de65985c3e07a743a84cda822a5ffb31980d39df13`  
		Last Modified: Mon, 08 Sep 2025 23:53:26 GMT  
		Size: 20.8 KB (20804 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:a97c783bb9e61ae8e7c7f8038e236fc6150abe9eca36ff0edaee0aee8b70920c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294659560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b214cc2238e49e232fecafca40cee02d5cfb266fc3faf3db364061d70b51e31`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c190eda88054318fcbdee78d8ef8cae137f19117a7e2bec8cc689ce5b64343`  
		Last Modified: Mon, 08 Sep 2025 23:53:48 GMT  
		Size: 42.3 MB (42270213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29205cde420f3386a6ec932407c0e575887fc341ae65db74ea280da3c6623f5`  
		Last Modified: Mon, 08 Sep 2025 22:25:11 GMT  
		Size: 1.6 MB (1566648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b121f20624a7437e0ea7c95f071379390a425cf722473abab14cd23cb34732`  
		Last Modified: Mon, 08 Sep 2025 23:53:51 GMT  
		Size: 220.7 MB (220686036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:297f008f6b5a02b796303bcff9642a65fd7849749ea887ccf39e3d8addc47ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c61a8b35b2aa67809ba8bdcc5eb7a48c23ea623044e44a13278599ea4374ee`

```dockerfile
```

-	Layers:
	-	`sha256:9a072058476f89d2d11b4b1e8f47b1501e0c353ae192e8928ecff1a605717089`  
		Last Modified: Mon, 08 Sep 2025 23:53:29 GMT  
		Size: 20.9 KB (20855 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; riscv64

```console
$ docker pull dart@sha256:a23a20664bad82073426026d01cd12f3f78729248a9a2b7fb3a1c3d7cfb709d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232352464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db3501795667e769c99accfe9399dd1d60358614edcd0644c96f5b1f122a121`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 27 Aug 2025 13:56:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 27 Aug 2025 13:56:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Aug 2025 13:56:45 GMT
WORKDIR /root
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f4927a3b04f70ec84088797f16339585618b2ec5aa5be4346e1db849de61a9`  
		Last Modified: Fri, 22 Aug 2025 03:19:46 GMT  
		Size: 41.5 MB (41549900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c103a39452af771458a8486e75d619bd52bca9bbf9f861f226f97afc19e70413`  
		Last Modified: Fri, 22 Aug 2025 03:19:42 GMT  
		Size: 1.6 MB (1567069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddcc9f0e9b433e088c2545cbd386786132bc494afa98bbf9cceb57617d2d367`  
		Last Modified: Fri, 29 Aug 2025 14:11:28 GMT  
		Size: 161.0 MB (160963840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:bce66f6d4297b47739c0954c0afb8a0d7ce89f167c49c26bb1aeb3183b4178d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d2a55131dba91a6d7993453feca1bc13eb3c878c7a270118bccf37a300adc0`

```dockerfile
```

-	Layers:
	-	`sha256:0082cc5e010b406fa5e9b523d55c695237a6177c1d766f114194870d8bf70c8e`  
		Last Modified: Fri, 29 Aug 2025 14:53:23 GMT  
		Size: 20.7 KB (20733 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:cc4d50f840b502dde7068fca505efedad0802817b15b78218b4512396717464a
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
$ docker pull dart@sha256:3e66cf04d5ede710f73734d83c49fe5f598729f668c4405e182642be071633d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295375890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d74785f94badad3736afeb4f7b76e9d43b4857aaafa417cea6b388f06959e30`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Sep 2025 11:42:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05c4aceb529f35f93eb6f1738babefcc3b2a7b2711d60e096f1460aa9f7dbae`  
		Last Modified: Mon, 08 Sep 2025 22:09:12 GMT  
		Size: 42.5 MB (42482593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677702b67ee1965df50e8ff7bab9200d6d743530e36e1b42449bbd70797ed751`  
		Last Modified: Mon, 08 Sep 2025 21:42:42 GMT  
		Size: 1.9 MB (1873612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e8b7557068bfac0eba4dd938e4106f62ce53b7dfe00f994ef29ee540375007`  
		Last Modified: Mon, 08 Sep 2025 22:09:11 GMT  
		Size: 221.2 MB (221246158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:57c77b466c4fdbc8b68d3e27de68f3c1ed005a8578d1337ccb4f79aaf16fc06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494a0f550d210d3f67be8f09d39f230732d45f2693dbb952b6da288add8c5f26`

```dockerfile
```

-	Layers:
	-	`sha256:e35e641e01735e6bbe594b05c7c452e632dd7974107ee3a3e6077d78a6f89af9`  
		Last Modified: Mon, 08 Sep 2025 23:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:34051496922f2a4ede768b1340880bdb586c93b08880e93fa0a9202efd6a385d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220750428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f328cd29cfc7c7bdbebb76a23f626c68f4dacf31e7ad16d3e00dad21f5437e`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56836f0c8e8c91ed8d9b18dcd856474127d1246651d41c7a7e1d85c5aa587e7`  
		Last Modified: Mon, 08 Sep 2025 23:12:50 GMT  
		Size: 37.5 MB (37478354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55445b8ad1d9275c46905f2852157c3dea0ba0d8318f4165761fdbc4a4d1804f`  
		Last Modified: Mon, 08 Sep 2025 22:47:12 GMT  
		Size: 1.3 MB (1275112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836ea90eeff7caed8d596d2ebd8d662040dac66c7d25e191612897e12c08911d`  
		Last Modified: Mon, 08 Sep 2025 23:12:42 GMT  
		Size: 155.8 MB (155789083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:0df9580b782efa5922674f248545627fa84db083825a4e488475bc2c245b2a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391e8aae71d36fc2f2abf20bf2fff2f507db492df051c3d7b57117589ed3c492`

```dockerfile
```

-	Layers:
	-	`sha256:061e9d6d0f6c9b75254d85de65985c3e07a743a84cda822a5ffb31980d39df13`  
		Last Modified: Mon, 08 Sep 2025 23:53:26 GMT  
		Size: 20.8 KB (20804 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:a97c783bb9e61ae8e7c7f8038e236fc6150abe9eca36ff0edaee0aee8b70920c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294659560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b214cc2238e49e232fecafca40cee02d5cfb266fc3faf3db364061d70b51e31`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c190eda88054318fcbdee78d8ef8cae137f19117a7e2bec8cc689ce5b64343`  
		Last Modified: Mon, 08 Sep 2025 23:53:48 GMT  
		Size: 42.3 MB (42270213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29205cde420f3386a6ec932407c0e575887fc341ae65db74ea280da3c6623f5`  
		Last Modified: Mon, 08 Sep 2025 22:25:11 GMT  
		Size: 1.6 MB (1566648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b121f20624a7437e0ea7c95f071379390a425cf722473abab14cd23cb34732`  
		Last Modified: Mon, 08 Sep 2025 23:53:51 GMT  
		Size: 220.7 MB (220686036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:297f008f6b5a02b796303bcff9642a65fd7849749ea887ccf39e3d8addc47ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c61a8b35b2aa67809ba8bdcc5eb7a48c23ea623044e44a13278599ea4374ee`

```dockerfile
```

-	Layers:
	-	`sha256:9a072058476f89d2d11b4b1e8f47b1501e0c353ae192e8928ecff1a605717089`  
		Last Modified: Mon, 08 Sep 2025 23:53:29 GMT  
		Size: 20.9 KB (20855 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; riscv64

```console
$ docker pull dart@sha256:a23a20664bad82073426026d01cd12f3f78729248a9a2b7fb3a1c3d7cfb709d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232352464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db3501795667e769c99accfe9399dd1d60358614edcd0644c96f5b1f122a121`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 27 Aug 2025 13:56:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 27 Aug 2025 13:56:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Aug 2025 13:56:45 GMT
WORKDIR /root
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f4927a3b04f70ec84088797f16339585618b2ec5aa5be4346e1db849de61a9`  
		Last Modified: Fri, 22 Aug 2025 03:19:46 GMT  
		Size: 41.5 MB (41549900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c103a39452af771458a8486e75d619bd52bca9bbf9f861f226f97afc19e70413`  
		Last Modified: Fri, 22 Aug 2025 03:19:42 GMT  
		Size: 1.6 MB (1567069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddcc9f0e9b433e088c2545cbd386786132bc494afa98bbf9cceb57617d2d367`  
		Last Modified: Fri, 29 Aug 2025 14:11:28 GMT  
		Size: 161.0 MB (160963840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:bce66f6d4297b47739c0954c0afb8a0d7ce89f167c49c26bb1aeb3183b4178d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d2a55131dba91a6d7993453feca1bc13eb3c878c7a270118bccf37a300adc0`

```dockerfile
```

-	Layers:
	-	`sha256:0082cc5e010b406fa5e9b523d55c695237a6177c1d766f114194870d8bf70c8e`  
		Last Modified: Fri, 29 Aug 2025 14:53:23 GMT  
		Size: 20.7 KB (20733 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:cc4d50f840b502dde7068fca505efedad0802817b15b78218b4512396717464a
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
$ docker pull dart@sha256:3e66cf04d5ede710f73734d83c49fe5f598729f668c4405e182642be071633d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295375890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d74785f94badad3736afeb4f7b76e9d43b4857aaafa417cea6b388f06959e30`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Sep 2025 11:42:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05c4aceb529f35f93eb6f1738babefcc3b2a7b2711d60e096f1460aa9f7dbae`  
		Last Modified: Mon, 08 Sep 2025 22:09:12 GMT  
		Size: 42.5 MB (42482593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677702b67ee1965df50e8ff7bab9200d6d743530e36e1b42449bbd70797ed751`  
		Last Modified: Mon, 08 Sep 2025 21:42:42 GMT  
		Size: 1.9 MB (1873612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e8b7557068bfac0eba4dd938e4106f62ce53b7dfe00f994ef29ee540375007`  
		Last Modified: Mon, 08 Sep 2025 22:09:11 GMT  
		Size: 221.2 MB (221246158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:57c77b466c4fdbc8b68d3e27de68f3c1ed005a8578d1337ccb4f79aaf16fc06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494a0f550d210d3f67be8f09d39f230732d45f2693dbb952b6da288add8c5f26`

```dockerfile
```

-	Layers:
	-	`sha256:e35e641e01735e6bbe594b05c7c452e632dd7974107ee3a3e6077d78a6f89af9`  
		Last Modified: Mon, 08 Sep 2025 23:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:34051496922f2a4ede768b1340880bdb586c93b08880e93fa0a9202efd6a385d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220750428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f328cd29cfc7c7bdbebb76a23f626c68f4dacf31e7ad16d3e00dad21f5437e`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56836f0c8e8c91ed8d9b18dcd856474127d1246651d41c7a7e1d85c5aa587e7`  
		Last Modified: Mon, 08 Sep 2025 23:12:50 GMT  
		Size: 37.5 MB (37478354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55445b8ad1d9275c46905f2852157c3dea0ba0d8318f4165761fdbc4a4d1804f`  
		Last Modified: Mon, 08 Sep 2025 22:47:12 GMT  
		Size: 1.3 MB (1275112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836ea90eeff7caed8d596d2ebd8d662040dac66c7d25e191612897e12c08911d`  
		Last Modified: Mon, 08 Sep 2025 23:12:42 GMT  
		Size: 155.8 MB (155789083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0df9580b782efa5922674f248545627fa84db083825a4e488475bc2c245b2a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391e8aae71d36fc2f2abf20bf2fff2f507db492df051c3d7b57117589ed3c492`

```dockerfile
```

-	Layers:
	-	`sha256:061e9d6d0f6c9b75254d85de65985c3e07a743a84cda822a5ffb31980d39df13`  
		Last Modified: Mon, 08 Sep 2025 23:53:26 GMT  
		Size: 20.8 KB (20804 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:a97c783bb9e61ae8e7c7f8038e236fc6150abe9eca36ff0edaee0aee8b70920c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294659560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b214cc2238e49e232fecafca40cee02d5cfb266fc3faf3db364061d70b51e31`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c190eda88054318fcbdee78d8ef8cae137f19117a7e2bec8cc689ce5b64343`  
		Last Modified: Mon, 08 Sep 2025 23:53:48 GMT  
		Size: 42.3 MB (42270213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29205cde420f3386a6ec932407c0e575887fc341ae65db74ea280da3c6623f5`  
		Last Modified: Mon, 08 Sep 2025 22:25:11 GMT  
		Size: 1.6 MB (1566648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b121f20624a7437e0ea7c95f071379390a425cf722473abab14cd23cb34732`  
		Last Modified: Mon, 08 Sep 2025 23:53:51 GMT  
		Size: 220.7 MB (220686036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:297f008f6b5a02b796303bcff9642a65fd7849749ea887ccf39e3d8addc47ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c61a8b35b2aa67809ba8bdcc5eb7a48c23ea623044e44a13278599ea4374ee`

```dockerfile
```

-	Layers:
	-	`sha256:9a072058476f89d2d11b4b1e8f47b1501e0c353ae192e8928ecff1a605717089`  
		Last Modified: Mon, 08 Sep 2025 23:53:29 GMT  
		Size: 20.9 KB (20855 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:a23a20664bad82073426026d01cd12f3f78729248a9a2b7fb3a1c3d7cfb709d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232352464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db3501795667e769c99accfe9399dd1d60358614edcd0644c96f5b1f122a121`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 27 Aug 2025 13:56:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 27 Aug 2025 13:56:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Aug 2025 13:56:45 GMT
WORKDIR /root
# Wed, 27 Aug 2025 13:56:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec22e81271582def81d3e10e2a555ae5d3d81c6951465a3d16cfc47938e9f92a;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b7d758f64ec94af2933a0d92238339eb9e179a0d61ebd4f9095ac675f4ad263;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d62f75f3f1bfb44a22fbd5cf0a5b47c758516ceca5dcc7bcec88896e2583e7ba;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f7a8c7ac419ef589fff5a1ca10a0dd7e3059c254fef065fb2f5b7a3f35e95217;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f4927a3b04f70ec84088797f16339585618b2ec5aa5be4346e1db849de61a9`  
		Last Modified: Fri, 22 Aug 2025 03:19:46 GMT  
		Size: 41.5 MB (41549900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c103a39452af771458a8486e75d619bd52bca9bbf9f861f226f97afc19e70413`  
		Last Modified: Fri, 22 Aug 2025 03:19:42 GMT  
		Size: 1.6 MB (1567069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddcc9f0e9b433e088c2545cbd386786132bc494afa98bbf9cceb57617d2d367`  
		Last Modified: Fri, 29 Aug 2025 14:11:28 GMT  
		Size: 161.0 MB (160963840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:bce66f6d4297b47739c0954c0afb8a0d7ce89f167c49c26bb1aeb3183b4178d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d2a55131dba91a6d7993453feca1bc13eb3c878c7a270118bccf37a300adc0`

```dockerfile
```

-	Layers:
	-	`sha256:0082cc5e010b406fa5e9b523d55c695237a6177c1d766f114194870d8bf70c8e`  
		Last Modified: Fri, 29 Aug 2025 14:53:23 GMT  
		Size: 20.7 KB (20733 bytes)  
		MIME: application/vnd.in-toto+json
