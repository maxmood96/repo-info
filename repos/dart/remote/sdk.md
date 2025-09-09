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
