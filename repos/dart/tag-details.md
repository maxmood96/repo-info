<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.10.0-75.2.beta`](#dart3100-752beta)
-	[`dart:3.10.0-75.2.beta-sdk`](#dart3100-752beta-sdk)
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
$ docker pull dart@sha256:43b7d9020d22e9ccaf013a7716e6c20e6da36da2872f70a4d36e025f7344fef5
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
$ docker pull dart@sha256:65060f22a0e187d589b30ffdd4553d994656ccd5bbe3473cd04b6bc9e48da116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295373459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555d91210e04c10028404b6fbb2952b7620b43565ab094abfa19291babd88782`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7611e74feb20851b1130bcc9bd8c0129e7c1c0e3b0020400d2332960f8854d7`  
		Last Modified: Wed, 27 Aug 2025 17:00:12 GMT  
		Size: 42.5 MB (42480136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46a9fcd5ad34d7175be17433da570662d17ffd30c35aff112b4f4b220c54b5d`  
		Last Modified: Wed, 27 Aug 2025 17:00:10 GMT  
		Size: 1.9 MB (1873606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f334ea837b6064ec27edd68df59a7ac0ba0648e73de671ece1a27781d18b6eff`  
		Last Modified: Wed, 27 Aug 2025 17:37:01 GMT  
		Size: 221.2 MB (221246400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:5af6dcf8512465f978cad26efa9eed38dddc3a43adcc73d83d5ed7787a56d428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba575a8886a3bcf3dfaf6c9aecae0032b256afba999424204647c92747f128e2`

```dockerfile
```

-	Layers:
	-	`sha256:281915cdd7a00d4d469d68b2d24d199d7e8cb9bb48527dc7be5fb85737d69729`  
		Last Modified: Wed, 27 Aug 2025 17:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:c0288fc72cdcac166021fdf1845a0df3102d67dc34bed12bac0f31770fa5a191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220750262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9aa78f3e944a684c7b5432a4e8fcbf775188c6004aaaf58f6227192928d6bd8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c057a1b1208d8b91ceb9c549498d8b1070ce4670a3db742f55a508f0e811363`  
		Last Modified: Wed, 27 Aug 2025 17:33:40 GMT  
		Size: 155.8 MB (155789217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:925849d43849db5c4887760f5d39f74cbb4ec1f1dd13dc007ee334095101c4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259ce88380f74e730a0c271ffc31a5cebabaaad844ffa6387e116a8111ea769a`

```dockerfile
```

-	Layers:
	-	`sha256:99f973603e81a94a6610825bc73afb1d7e26eb9bd1e8762fd695ff2322ed2c35`  
		Last Modified: Wed, 27 Aug 2025 17:53:27 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:eae202b79129653e9eba86aa2b7d937dbdee78a9eb6b9798879a76a3c2645868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294654235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffa61f59c0449760929123bb900bc4bfe585d16fbf6892e283f66a5ee30266e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9000d97bea06011816be9f25945ced50f31ad05eb520668404aeb0882fae5609`  
		Last Modified: Wed, 27 Aug 2025 17:00:20 GMT  
		Size: 42.3 MB (42265833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40d1be1d28b90af2e21ab46f813f59af74d9c0dd07026070203719fa487a1c9`  
		Last Modified: Wed, 27 Aug 2025 17:00:17 GMT  
		Size: 1.6 MB (1566651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5358a9be7b571d1319c47f66ddba7723cc565f0ff18de5d8f68742813ba1858d`  
		Last Modified: Wed, 27 Aug 2025 17:42:15 GMT  
		Size: 220.7 MB (220685675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:1f1f1730f412c0133590466bae8974592bc54f999f57a4dae2e86c2c16551a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45157eb41cdb24939321502d589ae9d53558366fe7fd1cd9b330df4bd3c417d`

```dockerfile
```

-	Layers:
	-	`sha256:c221b9c76de5333269e905ad5caa5622b86f9dd4c8fd1d184208873c69f321ec`  
		Last Modified: Wed, 27 Aug 2025 17:53:29 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; riscv64

```console
$ docker pull dart@sha256:f5302601d3823ec52c3b2227298e67a4a71cd07bab4a602a36c3c216af7ccf71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232350305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68799c58a6ba3ad3c460f348bfe1af139662e3b19455eaaadc827b1336c287c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
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
	-	`sha256:6c81a9390d0dea74d0dd5ee5f075ff9d4f75f5b1f488075fc37ae6501f9249d4`  
		Last Modified: Fri, 22 Aug 2025 05:53:45 GMT  
		Size: 161.0 MB (160961681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:b7c8ddd25637b499c8e7236faea5f000cf932d95912f032acf3e6bd18c8c7f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff44dbc8bcdd4e9fd31a3bc8b1291d0abecc7bb011589a4eb5d5eb8e76705e69`

```dockerfile
```

-	Layers:
	-	`sha256:7d474be0622a310b8fc874ca0973e5c9169478864a562a02cbd125139a56f1cb`  
		Last Modified: Fri, 22 Aug 2025 05:53:23 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:43b7d9020d22e9ccaf013a7716e6c20e6da36da2872f70a4d36e025f7344fef5
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
$ docker pull dart@sha256:65060f22a0e187d589b30ffdd4553d994656ccd5bbe3473cd04b6bc9e48da116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295373459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555d91210e04c10028404b6fbb2952b7620b43565ab094abfa19291babd88782`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7611e74feb20851b1130bcc9bd8c0129e7c1c0e3b0020400d2332960f8854d7`  
		Last Modified: Wed, 27 Aug 2025 17:00:12 GMT  
		Size: 42.5 MB (42480136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46a9fcd5ad34d7175be17433da570662d17ffd30c35aff112b4f4b220c54b5d`  
		Last Modified: Wed, 27 Aug 2025 17:00:10 GMT  
		Size: 1.9 MB (1873606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f334ea837b6064ec27edd68df59a7ac0ba0648e73de671ece1a27781d18b6eff`  
		Last Modified: Wed, 27 Aug 2025 17:37:01 GMT  
		Size: 221.2 MB (221246400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5af6dcf8512465f978cad26efa9eed38dddc3a43adcc73d83d5ed7787a56d428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba575a8886a3bcf3dfaf6c9aecae0032b256afba999424204647c92747f128e2`

```dockerfile
```

-	Layers:
	-	`sha256:281915cdd7a00d4d469d68b2d24d199d7e8cb9bb48527dc7be5fb85737d69729`  
		Last Modified: Wed, 27 Aug 2025 17:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:c0288fc72cdcac166021fdf1845a0df3102d67dc34bed12bac0f31770fa5a191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220750262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9aa78f3e944a684c7b5432a4e8fcbf775188c6004aaaf58f6227192928d6bd8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c057a1b1208d8b91ceb9c549498d8b1070ce4670a3db742f55a508f0e811363`  
		Last Modified: Wed, 27 Aug 2025 17:33:40 GMT  
		Size: 155.8 MB (155789217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:925849d43849db5c4887760f5d39f74cbb4ec1f1dd13dc007ee334095101c4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259ce88380f74e730a0c271ffc31a5cebabaaad844ffa6387e116a8111ea769a`

```dockerfile
```

-	Layers:
	-	`sha256:99f973603e81a94a6610825bc73afb1d7e26eb9bd1e8762fd695ff2322ed2c35`  
		Last Modified: Wed, 27 Aug 2025 17:53:27 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:eae202b79129653e9eba86aa2b7d937dbdee78a9eb6b9798879a76a3c2645868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294654235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffa61f59c0449760929123bb900bc4bfe585d16fbf6892e283f66a5ee30266e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9000d97bea06011816be9f25945ced50f31ad05eb520668404aeb0882fae5609`  
		Last Modified: Wed, 27 Aug 2025 17:00:20 GMT  
		Size: 42.3 MB (42265833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40d1be1d28b90af2e21ab46f813f59af74d9c0dd07026070203719fa487a1c9`  
		Last Modified: Wed, 27 Aug 2025 17:00:17 GMT  
		Size: 1.6 MB (1566651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5358a9be7b571d1319c47f66ddba7723cc565f0ff18de5d8f68742813ba1858d`  
		Last Modified: Wed, 27 Aug 2025 17:42:15 GMT  
		Size: 220.7 MB (220685675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1f1f1730f412c0133590466bae8974592bc54f999f57a4dae2e86c2c16551a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45157eb41cdb24939321502d589ae9d53558366fe7fd1cd9b330df4bd3c417d`

```dockerfile
```

-	Layers:
	-	`sha256:c221b9c76de5333269e905ad5caa5622b86f9dd4c8fd1d184208873c69f321ec`  
		Last Modified: Wed, 27 Aug 2025 17:53:29 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:f5302601d3823ec52c3b2227298e67a4a71cd07bab4a602a36c3c216af7ccf71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232350305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68799c58a6ba3ad3c460f348bfe1af139662e3b19455eaaadc827b1336c287c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
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
	-	`sha256:6c81a9390d0dea74d0dd5ee5f075ff9d4f75f5b1f488075fc37ae6501f9249d4`  
		Last Modified: Fri, 22 Aug 2025 05:53:45 GMT  
		Size: 161.0 MB (160961681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b7c8ddd25637b499c8e7236faea5f000cf932d95912f032acf3e6bd18c8c7f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff44dbc8bcdd4e9fd31a3bc8b1291d0abecc7bb011589a4eb5d5eb8e76705e69`

```dockerfile
```

-	Layers:
	-	`sha256:7d474be0622a310b8fc874ca0973e5c9169478864a562a02cbd125139a56f1cb`  
		Last Modified: Fri, 22 Aug 2025 05:53:23 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.0-75.2.beta`

```console
$ docker pull dart@sha256:8d420909c1446d55c76870c77cf9dcf7ae6efd5243e94e56d7d0083a5fea52c8
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

### `dart:3.10.0-75.2.beta` - linux; amd64

```console
$ docker pull dart@sha256:b6378c512ec83f5eca5f5fce2273fcdb8994d0b5b5c20785204269aa64857145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282051742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73772d903bce62e961e7f57a0e24cd37f59cfcb2abc3ae3ff6f366d90e850b38`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38957d8c988c1b2918c2851da073d829ed717aed6c20a0db7c765970e4454eb7`  
		Last Modified: Wed, 20 Aug 2025 18:40:49 GMT  
		Size: 42.5 MB (42480170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67608fd3791b8b8ed71ae6b23139605d68d89a91694d98ed76b884a527be5e61`  
		Last Modified: Wed, 20 Aug 2025 18:40:44 GMT  
		Size: 1.9 MB (1873607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a809654f230d0f007cc01cb902ea5a09d387bafd46a6602a0b914f96b9784e1`  
		Last Modified: Wed, 20 Aug 2025 20:54:06 GMT  
		Size: 207.9 MB (207924648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-75.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:4dc57f26035f8dc52c2e45dabd6078585da8166099282623161725993e8edd2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3f0e94468d41f8eba6af03807e16bc677a900e68f8429c353832396b7601f3`

```dockerfile
```

-	Layers:
	-	`sha256:f0e9246662234c3fc1435b0f1ba767acc50b73604b03eb13c3cbb642f3b39b99`  
		Last Modified: Wed, 20 Aug 2025 20:53:35 GMT  
		Size: 19.0 KB (18961 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-75.2.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:bb46ce3f842d3e3ad8a72df540071b5f14447a5e23c655d989215d773be460ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215046111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9d30927b42ac20f74ccd8f91ab91d4c3727b6730639befebce1c7f0d144b76`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab492f2b844ab0e6b83f1dc61379567ed6a187423e24cec259e149feb4e4ab7`  
		Last Modified: Wed, 20 Aug 2025 20:54:03 GMT  
		Size: 150.1 MB (150085066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-75.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:0b86c429573db488866051100a0ee632d741e53055907ab493fc41060f16aad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cfe09089a4f3219c68e4b394b1be7050c1f0d390e7a77b39e69bf84a046622`

```dockerfile
```

-	Layers:
	-	`sha256:4e19f7e18f207d87738b361b1ca6f8302f261685c106c5a6661d8e51c60bfeb9`  
		Last Modified: Wed, 20 Aug 2025 20:53:39 GMT  
		Size: 19.1 KB (19063 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-75.2.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d9e367080af7d7a6a57f2781f4333dbd9005d26f548ebc29fe1450190e10834f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281265106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fadbfae3509bbf907a973d7280590d1150a03a20cb3cab8c369cc9239c3988`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3afea05610d5e523abc7b1b80da95f86be166605de4bc50f647f30021609db`  
		Last Modified: Wed, 20 Aug 2025 18:52:15 GMT  
		Size: 42.3 MB (42265724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6856a5741073f9a038c6f208b8b8c66a087d92e3f8d612594b31b217d6ae444c`  
		Last Modified: Wed, 20 Aug 2025 18:52:11 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24702d5295002e9267969550b7c98f0c74f8875fcae5a97f82eae1fb8e5b650`  
		Last Modified: Wed, 20 Aug 2025 20:54:14 GMT  
		Size: 207.3 MB (207296661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-75.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:7eeaa1f52aec4062754c686bd18467badb4ec5c00aedc1064875a2e139c209bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05292d6b123362939cc2dd9bfed071412be258ccfdb530ae71e2f4fd0460ce61`

```dockerfile
```

-	Layers:
	-	`sha256:aaeefecd88aeccafb0315f2b0305431275103d192379b42d10e06b20294a3a87`  
		Last Modified: Wed, 20 Aug 2025 20:53:42 GMT  
		Size: 19.1 KB (19095 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-75.2.beta` - linux; riscv64

```console
$ docker pull dart@sha256:77440ee296dc4830f12f10faadb63b33d70f7e4b5406c9cda9590745e3529ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228193385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43adbe7867b239884bd232412ede9633651568e4a8d55064d322ef4487d4a186`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
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
	-	`sha256:6c021fe7c34d21d36f48e05c739e0f12bb23c30ad7bc32bb246b729ee596cbb5`  
		Last Modified: Fri, 22 Aug 2025 05:53:52 GMT  
		Size: 156.8 MB (156804761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-75.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:e515ae92445233ad355e5121ec899544ecd520cf711d5c516e2739e03c37f241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d4203225c76bee9800e08281ff6703b7c055fcc90e2009e3ea7140fd0e6648`

```dockerfile
```

-	Layers:
	-	`sha256:43bb18047c17426808937209753c9a0b282b83b12d69727b974166763407691d`  
		Last Modified: Fri, 22 Aug 2025 05:53:30 GMT  
		Size: 19.0 KB (19009 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.0-75.2.beta-sdk`

```console
$ docker pull dart@sha256:8d420909c1446d55c76870c77cf9dcf7ae6efd5243e94e56d7d0083a5fea52c8
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

### `dart:3.10.0-75.2.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:b6378c512ec83f5eca5f5fce2273fcdb8994d0b5b5c20785204269aa64857145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282051742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73772d903bce62e961e7f57a0e24cd37f59cfcb2abc3ae3ff6f366d90e850b38`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38957d8c988c1b2918c2851da073d829ed717aed6c20a0db7c765970e4454eb7`  
		Last Modified: Wed, 20 Aug 2025 18:40:49 GMT  
		Size: 42.5 MB (42480170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67608fd3791b8b8ed71ae6b23139605d68d89a91694d98ed76b884a527be5e61`  
		Last Modified: Wed, 20 Aug 2025 18:40:44 GMT  
		Size: 1.9 MB (1873607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a809654f230d0f007cc01cb902ea5a09d387bafd46a6602a0b914f96b9784e1`  
		Last Modified: Wed, 20 Aug 2025 20:54:06 GMT  
		Size: 207.9 MB (207924648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-75.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4dc57f26035f8dc52c2e45dabd6078585da8166099282623161725993e8edd2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3f0e94468d41f8eba6af03807e16bc677a900e68f8429c353832396b7601f3`

```dockerfile
```

-	Layers:
	-	`sha256:f0e9246662234c3fc1435b0f1ba767acc50b73604b03eb13c3cbb642f3b39b99`  
		Last Modified: Wed, 20 Aug 2025 20:53:35 GMT  
		Size: 19.0 KB (18961 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-75.2.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:bb46ce3f842d3e3ad8a72df540071b5f14447a5e23c655d989215d773be460ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215046111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9d30927b42ac20f74ccd8f91ab91d4c3727b6730639befebce1c7f0d144b76`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab492f2b844ab0e6b83f1dc61379567ed6a187423e24cec259e149feb4e4ab7`  
		Last Modified: Wed, 20 Aug 2025 20:54:03 GMT  
		Size: 150.1 MB (150085066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-75.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0b86c429573db488866051100a0ee632d741e53055907ab493fc41060f16aad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cfe09089a4f3219c68e4b394b1be7050c1f0d390e7a77b39e69bf84a046622`

```dockerfile
```

-	Layers:
	-	`sha256:4e19f7e18f207d87738b361b1ca6f8302f261685c106c5a6661d8e51c60bfeb9`  
		Last Modified: Wed, 20 Aug 2025 20:53:39 GMT  
		Size: 19.1 KB (19063 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-75.2.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d9e367080af7d7a6a57f2781f4333dbd9005d26f548ebc29fe1450190e10834f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281265106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fadbfae3509bbf907a973d7280590d1150a03a20cb3cab8c369cc9239c3988`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3afea05610d5e523abc7b1b80da95f86be166605de4bc50f647f30021609db`  
		Last Modified: Wed, 20 Aug 2025 18:52:15 GMT  
		Size: 42.3 MB (42265724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6856a5741073f9a038c6f208b8b8c66a087d92e3f8d612594b31b217d6ae444c`  
		Last Modified: Wed, 20 Aug 2025 18:52:11 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24702d5295002e9267969550b7c98f0c74f8875fcae5a97f82eae1fb8e5b650`  
		Last Modified: Wed, 20 Aug 2025 20:54:14 GMT  
		Size: 207.3 MB (207296661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-75.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7eeaa1f52aec4062754c686bd18467badb4ec5c00aedc1064875a2e139c209bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05292d6b123362939cc2dd9bfed071412be258ccfdb530ae71e2f4fd0460ce61`

```dockerfile
```

-	Layers:
	-	`sha256:aaeefecd88aeccafb0315f2b0305431275103d192379b42d10e06b20294a3a87`  
		Last Modified: Wed, 20 Aug 2025 20:53:42 GMT  
		Size: 19.1 KB (19095 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-75.2.beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:77440ee296dc4830f12f10faadb63b33d70f7e4b5406c9cda9590745e3529ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228193385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43adbe7867b239884bd232412ede9633651568e4a8d55064d322ef4487d4a186`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
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
	-	`sha256:6c021fe7c34d21d36f48e05c739e0f12bb23c30ad7bc32bb246b729ee596cbb5`  
		Last Modified: Fri, 22 Aug 2025 05:53:52 GMT  
		Size: 156.8 MB (156804761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-75.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e515ae92445233ad355e5121ec899544ecd520cf711d5c516e2739e03c37f241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d4203225c76bee9800e08281ff6703b7c055fcc90e2009e3ea7140fd0e6648`

```dockerfile
```

-	Layers:
	-	`sha256:43bb18047c17426808937209753c9a0b282b83b12d69727b974166763407691d`  
		Last Modified: Fri, 22 Aug 2025 05:53:30 GMT  
		Size: 19.0 KB (19009 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9`

```console
$ docker pull dart@sha256:43b7d9020d22e9ccaf013a7716e6c20e6da36da2872f70a4d36e025f7344fef5
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
$ docker pull dart@sha256:65060f22a0e187d589b30ffdd4553d994656ccd5bbe3473cd04b6bc9e48da116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295373459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555d91210e04c10028404b6fbb2952b7620b43565ab094abfa19291babd88782`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7611e74feb20851b1130bcc9bd8c0129e7c1c0e3b0020400d2332960f8854d7`  
		Last Modified: Wed, 27 Aug 2025 17:00:12 GMT  
		Size: 42.5 MB (42480136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46a9fcd5ad34d7175be17433da570662d17ffd30c35aff112b4f4b220c54b5d`  
		Last Modified: Wed, 27 Aug 2025 17:00:10 GMT  
		Size: 1.9 MB (1873606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f334ea837b6064ec27edd68df59a7ac0ba0648e73de671ece1a27781d18b6eff`  
		Last Modified: Wed, 27 Aug 2025 17:37:01 GMT  
		Size: 221.2 MB (221246400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:5af6dcf8512465f978cad26efa9eed38dddc3a43adcc73d83d5ed7787a56d428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba575a8886a3bcf3dfaf6c9aecae0032b256afba999424204647c92747f128e2`

```dockerfile
```

-	Layers:
	-	`sha256:281915cdd7a00d4d469d68b2d24d199d7e8cb9bb48527dc7be5fb85737d69729`  
		Last Modified: Wed, 27 Aug 2025 17:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9` - linux; arm variant v7

```console
$ docker pull dart@sha256:c0288fc72cdcac166021fdf1845a0df3102d67dc34bed12bac0f31770fa5a191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220750262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9aa78f3e944a684c7b5432a4e8fcbf775188c6004aaaf58f6227192928d6bd8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c057a1b1208d8b91ceb9c549498d8b1070ce4670a3db742f55a508f0e811363`  
		Last Modified: Wed, 27 Aug 2025 17:33:40 GMT  
		Size: 155.8 MB (155789217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:925849d43849db5c4887760f5d39f74cbb4ec1f1dd13dc007ee334095101c4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259ce88380f74e730a0c271ffc31a5cebabaaad844ffa6387e116a8111ea769a`

```dockerfile
```

-	Layers:
	-	`sha256:99f973603e81a94a6610825bc73afb1d7e26eb9bd1e8762fd695ff2322ed2c35`  
		Last Modified: Wed, 27 Aug 2025 17:53:27 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:eae202b79129653e9eba86aa2b7d937dbdee78a9eb6b9798879a76a3c2645868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294654235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffa61f59c0449760929123bb900bc4bfe585d16fbf6892e283f66a5ee30266e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9000d97bea06011816be9f25945ced50f31ad05eb520668404aeb0882fae5609`  
		Last Modified: Wed, 27 Aug 2025 17:00:20 GMT  
		Size: 42.3 MB (42265833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40d1be1d28b90af2e21ab46f813f59af74d9c0dd07026070203719fa487a1c9`  
		Last Modified: Wed, 27 Aug 2025 17:00:17 GMT  
		Size: 1.6 MB (1566651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5358a9be7b571d1319c47f66ddba7723cc565f0ff18de5d8f68742813ba1858d`  
		Last Modified: Wed, 27 Aug 2025 17:42:15 GMT  
		Size: 220.7 MB (220685675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:1f1f1730f412c0133590466bae8974592bc54f999f57a4dae2e86c2c16551a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45157eb41cdb24939321502d589ae9d53558366fe7fd1cd9b330df4bd3c417d`

```dockerfile
```

-	Layers:
	-	`sha256:c221b9c76de5333269e905ad5caa5622b86f9dd4c8fd1d184208873c69f321ec`  
		Last Modified: Wed, 27 Aug 2025 17:53:29 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9` - linux; riscv64

```console
$ docker pull dart@sha256:f5302601d3823ec52c3b2227298e67a4a71cd07bab4a602a36c3c216af7ccf71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232350305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68799c58a6ba3ad3c460f348bfe1af139662e3b19455eaaadc827b1336c287c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
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
	-	`sha256:6c81a9390d0dea74d0dd5ee5f075ff9d4f75f5b1f488075fc37ae6501f9249d4`  
		Last Modified: Fri, 22 Aug 2025 05:53:45 GMT  
		Size: 161.0 MB (160961681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:b7c8ddd25637b499c8e7236faea5f000cf932d95912f032acf3e6bd18c8c7f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff44dbc8bcdd4e9fd31a3bc8b1291d0abecc7bb011589a4eb5d5eb8e76705e69`

```dockerfile
```

-	Layers:
	-	`sha256:7d474be0622a310b8fc874ca0973e5c9169478864a562a02cbd125139a56f1cb`  
		Last Modified: Fri, 22 Aug 2025 05:53:23 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9-sdk`

```console
$ docker pull dart@sha256:43b7d9020d22e9ccaf013a7716e6c20e6da36da2872f70a4d36e025f7344fef5
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
$ docker pull dart@sha256:65060f22a0e187d589b30ffdd4553d994656ccd5bbe3473cd04b6bc9e48da116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295373459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555d91210e04c10028404b6fbb2952b7620b43565ab094abfa19291babd88782`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7611e74feb20851b1130bcc9bd8c0129e7c1c0e3b0020400d2332960f8854d7`  
		Last Modified: Wed, 27 Aug 2025 17:00:12 GMT  
		Size: 42.5 MB (42480136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46a9fcd5ad34d7175be17433da570662d17ffd30c35aff112b4f4b220c54b5d`  
		Last Modified: Wed, 27 Aug 2025 17:00:10 GMT  
		Size: 1.9 MB (1873606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f334ea837b6064ec27edd68df59a7ac0ba0648e73de671ece1a27781d18b6eff`  
		Last Modified: Wed, 27 Aug 2025 17:37:01 GMT  
		Size: 221.2 MB (221246400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5af6dcf8512465f978cad26efa9eed38dddc3a43adcc73d83d5ed7787a56d428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba575a8886a3bcf3dfaf6c9aecae0032b256afba999424204647c92747f128e2`

```dockerfile
```

-	Layers:
	-	`sha256:281915cdd7a00d4d469d68b2d24d199d7e8cb9bb48527dc7be5fb85737d69729`  
		Last Modified: Wed, 27 Aug 2025 17:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:c0288fc72cdcac166021fdf1845a0df3102d67dc34bed12bac0f31770fa5a191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220750262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9aa78f3e944a684c7b5432a4e8fcbf775188c6004aaaf58f6227192928d6bd8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c057a1b1208d8b91ceb9c549498d8b1070ce4670a3db742f55a508f0e811363`  
		Last Modified: Wed, 27 Aug 2025 17:33:40 GMT  
		Size: 155.8 MB (155789217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:925849d43849db5c4887760f5d39f74cbb4ec1f1dd13dc007ee334095101c4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259ce88380f74e730a0c271ffc31a5cebabaaad844ffa6387e116a8111ea769a`

```dockerfile
```

-	Layers:
	-	`sha256:99f973603e81a94a6610825bc73afb1d7e26eb9bd1e8762fd695ff2322ed2c35`  
		Last Modified: Wed, 27 Aug 2025 17:53:27 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:eae202b79129653e9eba86aa2b7d937dbdee78a9eb6b9798879a76a3c2645868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294654235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffa61f59c0449760929123bb900bc4bfe585d16fbf6892e283f66a5ee30266e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9000d97bea06011816be9f25945ced50f31ad05eb520668404aeb0882fae5609`  
		Last Modified: Wed, 27 Aug 2025 17:00:20 GMT  
		Size: 42.3 MB (42265833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40d1be1d28b90af2e21ab46f813f59af74d9c0dd07026070203719fa487a1c9`  
		Last Modified: Wed, 27 Aug 2025 17:00:17 GMT  
		Size: 1.6 MB (1566651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5358a9be7b571d1319c47f66ddba7723cc565f0ff18de5d8f68742813ba1858d`  
		Last Modified: Wed, 27 Aug 2025 17:42:15 GMT  
		Size: 220.7 MB (220685675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1f1f1730f412c0133590466bae8974592bc54f999f57a4dae2e86c2c16551a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45157eb41cdb24939321502d589ae9d53558366fe7fd1cd9b330df4bd3c417d`

```dockerfile
```

-	Layers:
	-	`sha256:c221b9c76de5333269e905ad5caa5622b86f9dd4c8fd1d184208873c69f321ec`  
		Last Modified: Wed, 27 Aug 2025 17:53:29 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:f5302601d3823ec52c3b2227298e67a4a71cd07bab4a602a36c3c216af7ccf71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232350305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68799c58a6ba3ad3c460f348bfe1af139662e3b19455eaaadc827b1336c287c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
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
	-	`sha256:6c81a9390d0dea74d0dd5ee5f075ff9d4f75f5b1f488075fc37ae6501f9249d4`  
		Last Modified: Fri, 22 Aug 2025 05:53:45 GMT  
		Size: 161.0 MB (160961681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b7c8ddd25637b499c8e7236faea5f000cf932d95912f032acf3e6bd18c8c7f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff44dbc8bcdd4e9fd31a3bc8b1291d0abecc7bb011589a4eb5d5eb8e76705e69`

```dockerfile
```

-	Layers:
	-	`sha256:7d474be0622a310b8fc874ca0973e5c9169478864a562a02cbd125139a56f1cb`  
		Last Modified: Fri, 22 Aug 2025 05:53:23 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9.2`

```console
$ docker pull dart@sha256:95a6ad351923a9579306824d0d271e4632d351dbb71bb1410ed3433c12d3d162
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.9.2` - linux; amd64

```console
$ docker pull dart@sha256:65060f22a0e187d589b30ffdd4553d994656ccd5bbe3473cd04b6bc9e48da116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295373459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555d91210e04c10028404b6fbb2952b7620b43565ab094abfa19291babd88782`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7611e74feb20851b1130bcc9bd8c0129e7c1c0e3b0020400d2332960f8854d7`  
		Last Modified: Wed, 27 Aug 2025 17:00:12 GMT  
		Size: 42.5 MB (42480136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46a9fcd5ad34d7175be17433da570662d17ffd30c35aff112b4f4b220c54b5d`  
		Last Modified: Wed, 27 Aug 2025 17:00:10 GMT  
		Size: 1.9 MB (1873606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f334ea837b6064ec27edd68df59a7ac0ba0648e73de671ece1a27781d18b6eff`  
		Last Modified: Wed, 27 Aug 2025 17:37:01 GMT  
		Size: 221.2 MB (221246400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.2` - unknown; unknown

```console
$ docker pull dart@sha256:5af6dcf8512465f978cad26efa9eed38dddc3a43adcc73d83d5ed7787a56d428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba575a8886a3bcf3dfaf6c9aecae0032b256afba999424204647c92747f128e2`

```dockerfile
```

-	Layers:
	-	`sha256:281915cdd7a00d4d469d68b2d24d199d7e8cb9bb48527dc7be5fb85737d69729`  
		Last Modified: Wed, 27 Aug 2025 17:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.2` - linux; arm variant v7

```console
$ docker pull dart@sha256:c0288fc72cdcac166021fdf1845a0df3102d67dc34bed12bac0f31770fa5a191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220750262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9aa78f3e944a684c7b5432a4e8fcbf775188c6004aaaf58f6227192928d6bd8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c057a1b1208d8b91ceb9c549498d8b1070ce4670a3db742f55a508f0e811363`  
		Last Modified: Wed, 27 Aug 2025 17:33:40 GMT  
		Size: 155.8 MB (155789217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.2` - unknown; unknown

```console
$ docker pull dart@sha256:925849d43849db5c4887760f5d39f74cbb4ec1f1dd13dc007ee334095101c4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259ce88380f74e730a0c271ffc31a5cebabaaad844ffa6387e116a8111ea769a`

```dockerfile
```

-	Layers:
	-	`sha256:99f973603e81a94a6610825bc73afb1d7e26eb9bd1e8762fd695ff2322ed2c35`  
		Last Modified: Wed, 27 Aug 2025 17:53:27 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.2` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:eae202b79129653e9eba86aa2b7d937dbdee78a9eb6b9798879a76a3c2645868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294654235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffa61f59c0449760929123bb900bc4bfe585d16fbf6892e283f66a5ee30266e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9000d97bea06011816be9f25945ced50f31ad05eb520668404aeb0882fae5609`  
		Last Modified: Wed, 27 Aug 2025 17:00:20 GMT  
		Size: 42.3 MB (42265833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40d1be1d28b90af2e21ab46f813f59af74d9c0dd07026070203719fa487a1c9`  
		Last Modified: Wed, 27 Aug 2025 17:00:17 GMT  
		Size: 1.6 MB (1566651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5358a9be7b571d1319c47f66ddba7723cc565f0ff18de5d8f68742813ba1858d`  
		Last Modified: Wed, 27 Aug 2025 17:42:15 GMT  
		Size: 220.7 MB (220685675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.2` - unknown; unknown

```console
$ docker pull dart@sha256:1f1f1730f412c0133590466bae8974592bc54f999f57a4dae2e86c2c16551a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45157eb41cdb24939321502d589ae9d53558366fe7fd1cd9b330df4bd3c417d`

```dockerfile
```

-	Layers:
	-	`sha256:c221b9c76de5333269e905ad5caa5622b86f9dd4c8fd1d184208873c69f321ec`  
		Last Modified: Wed, 27 Aug 2025 17:53:29 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9.2-sdk`

```console
$ docker pull dart@sha256:95a6ad351923a9579306824d0d271e4632d351dbb71bb1410ed3433c12d3d162
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.9.2-sdk` - linux; amd64

```console
$ docker pull dart@sha256:65060f22a0e187d589b30ffdd4553d994656ccd5bbe3473cd04b6bc9e48da116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295373459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555d91210e04c10028404b6fbb2952b7620b43565ab094abfa19291babd88782`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7611e74feb20851b1130bcc9bd8c0129e7c1c0e3b0020400d2332960f8854d7`  
		Last Modified: Wed, 27 Aug 2025 17:00:12 GMT  
		Size: 42.5 MB (42480136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46a9fcd5ad34d7175be17433da570662d17ffd30c35aff112b4f4b220c54b5d`  
		Last Modified: Wed, 27 Aug 2025 17:00:10 GMT  
		Size: 1.9 MB (1873606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f334ea837b6064ec27edd68df59a7ac0ba0648e73de671ece1a27781d18b6eff`  
		Last Modified: Wed, 27 Aug 2025 17:37:01 GMT  
		Size: 221.2 MB (221246400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.2-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5af6dcf8512465f978cad26efa9eed38dddc3a43adcc73d83d5ed7787a56d428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba575a8886a3bcf3dfaf6c9aecae0032b256afba999424204647c92747f128e2`

```dockerfile
```

-	Layers:
	-	`sha256:281915cdd7a00d4d469d68b2d24d199d7e8cb9bb48527dc7be5fb85737d69729`  
		Last Modified: Wed, 27 Aug 2025 17:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.2-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:c0288fc72cdcac166021fdf1845a0df3102d67dc34bed12bac0f31770fa5a191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220750262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9aa78f3e944a684c7b5432a4e8fcbf775188c6004aaaf58f6227192928d6bd8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c057a1b1208d8b91ceb9c549498d8b1070ce4670a3db742f55a508f0e811363`  
		Last Modified: Wed, 27 Aug 2025 17:33:40 GMT  
		Size: 155.8 MB (155789217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.2-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:925849d43849db5c4887760f5d39f74cbb4ec1f1dd13dc007ee334095101c4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259ce88380f74e730a0c271ffc31a5cebabaaad844ffa6387e116a8111ea769a`

```dockerfile
```

-	Layers:
	-	`sha256:99f973603e81a94a6610825bc73afb1d7e26eb9bd1e8762fd695ff2322ed2c35`  
		Last Modified: Wed, 27 Aug 2025 17:53:27 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.2-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:eae202b79129653e9eba86aa2b7d937dbdee78a9eb6b9798879a76a3c2645868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294654235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffa61f59c0449760929123bb900bc4bfe585d16fbf6892e283f66a5ee30266e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9000d97bea06011816be9f25945ced50f31ad05eb520668404aeb0882fae5609`  
		Last Modified: Wed, 27 Aug 2025 17:00:20 GMT  
		Size: 42.3 MB (42265833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40d1be1d28b90af2e21ab46f813f59af74d9c0dd07026070203719fa487a1c9`  
		Last Modified: Wed, 27 Aug 2025 17:00:17 GMT  
		Size: 1.6 MB (1566651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5358a9be7b571d1319c47f66ddba7723cc565f0ff18de5d8f68742813ba1858d`  
		Last Modified: Wed, 27 Aug 2025 17:42:15 GMT  
		Size: 220.7 MB (220685675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.2-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1f1f1730f412c0133590466bae8974592bc54f999f57a4dae2e86c2c16551a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45157eb41cdb24939321502d589ae9d53558366fe7fd1cd9b330df4bd3c417d`

```dockerfile
```

-	Layers:
	-	`sha256:c221b9c76de5333269e905ad5caa5622b86f9dd4c8fd1d184208873c69f321ec`  
		Last Modified: Wed, 27 Aug 2025 17:53:29 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:8d420909c1446d55c76870c77cf9dcf7ae6efd5243e94e56d7d0083a5fea52c8
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
$ docker pull dart@sha256:b6378c512ec83f5eca5f5fce2273fcdb8994d0b5b5c20785204269aa64857145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282051742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73772d903bce62e961e7f57a0e24cd37f59cfcb2abc3ae3ff6f366d90e850b38`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38957d8c988c1b2918c2851da073d829ed717aed6c20a0db7c765970e4454eb7`  
		Last Modified: Wed, 20 Aug 2025 18:40:49 GMT  
		Size: 42.5 MB (42480170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67608fd3791b8b8ed71ae6b23139605d68d89a91694d98ed76b884a527be5e61`  
		Last Modified: Wed, 20 Aug 2025 18:40:44 GMT  
		Size: 1.9 MB (1873607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a809654f230d0f007cc01cb902ea5a09d387bafd46a6602a0b914f96b9784e1`  
		Last Modified: Wed, 20 Aug 2025 20:54:06 GMT  
		Size: 207.9 MB (207924648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:4dc57f26035f8dc52c2e45dabd6078585da8166099282623161725993e8edd2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3f0e94468d41f8eba6af03807e16bc677a900e68f8429c353832396b7601f3`

```dockerfile
```

-	Layers:
	-	`sha256:f0e9246662234c3fc1435b0f1ba767acc50b73604b03eb13c3cbb642f3b39b99`  
		Last Modified: Wed, 20 Aug 2025 20:53:35 GMT  
		Size: 19.0 KB (18961 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:bb46ce3f842d3e3ad8a72df540071b5f14447a5e23c655d989215d773be460ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215046111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9d30927b42ac20f74ccd8f91ab91d4c3727b6730639befebce1c7f0d144b76`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab492f2b844ab0e6b83f1dc61379567ed6a187423e24cec259e149feb4e4ab7`  
		Last Modified: Wed, 20 Aug 2025 20:54:03 GMT  
		Size: 150.1 MB (150085066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:0b86c429573db488866051100a0ee632d741e53055907ab493fc41060f16aad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cfe09089a4f3219c68e4b394b1be7050c1f0d390e7a77b39e69bf84a046622`

```dockerfile
```

-	Layers:
	-	`sha256:4e19f7e18f207d87738b361b1ca6f8302f261685c106c5a6661d8e51c60bfeb9`  
		Last Modified: Wed, 20 Aug 2025 20:53:39 GMT  
		Size: 19.1 KB (19063 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d9e367080af7d7a6a57f2781f4333dbd9005d26f548ebc29fe1450190e10834f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281265106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fadbfae3509bbf907a973d7280590d1150a03a20cb3cab8c369cc9239c3988`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3afea05610d5e523abc7b1b80da95f86be166605de4bc50f647f30021609db`  
		Last Modified: Wed, 20 Aug 2025 18:52:15 GMT  
		Size: 42.3 MB (42265724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6856a5741073f9a038c6f208b8b8c66a087d92e3f8d612594b31b217d6ae444c`  
		Last Modified: Wed, 20 Aug 2025 18:52:11 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24702d5295002e9267969550b7c98f0c74f8875fcae5a97f82eae1fb8e5b650`  
		Last Modified: Wed, 20 Aug 2025 20:54:14 GMT  
		Size: 207.3 MB (207296661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:7eeaa1f52aec4062754c686bd18467badb4ec5c00aedc1064875a2e139c209bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05292d6b123362939cc2dd9bfed071412be258ccfdb530ae71e2f4fd0460ce61`

```dockerfile
```

-	Layers:
	-	`sha256:aaeefecd88aeccafb0315f2b0305431275103d192379b42d10e06b20294a3a87`  
		Last Modified: Wed, 20 Aug 2025 20:53:42 GMT  
		Size: 19.1 KB (19095 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:77440ee296dc4830f12f10faadb63b33d70f7e4b5406c9cda9590745e3529ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228193385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43adbe7867b239884bd232412ede9633651568e4a8d55064d322ef4487d4a186`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
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
	-	`sha256:6c021fe7c34d21d36f48e05c739e0f12bb23c30ad7bc32bb246b729ee596cbb5`  
		Last Modified: Fri, 22 Aug 2025 05:53:52 GMT  
		Size: 156.8 MB (156804761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:e515ae92445233ad355e5121ec899544ecd520cf711d5c516e2739e03c37f241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d4203225c76bee9800e08281ff6703b7c055fcc90e2009e3ea7140fd0e6648`

```dockerfile
```

-	Layers:
	-	`sha256:43bb18047c17426808937209753c9a0b282b83b12d69727b974166763407691d`  
		Last Modified: Fri, 22 Aug 2025 05:53:30 GMT  
		Size: 19.0 KB (19009 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:8d420909c1446d55c76870c77cf9dcf7ae6efd5243e94e56d7d0083a5fea52c8
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
$ docker pull dart@sha256:b6378c512ec83f5eca5f5fce2273fcdb8994d0b5b5c20785204269aa64857145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282051742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73772d903bce62e961e7f57a0e24cd37f59cfcb2abc3ae3ff6f366d90e850b38`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38957d8c988c1b2918c2851da073d829ed717aed6c20a0db7c765970e4454eb7`  
		Last Modified: Wed, 20 Aug 2025 18:40:49 GMT  
		Size: 42.5 MB (42480170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67608fd3791b8b8ed71ae6b23139605d68d89a91694d98ed76b884a527be5e61`  
		Last Modified: Wed, 20 Aug 2025 18:40:44 GMT  
		Size: 1.9 MB (1873607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a809654f230d0f007cc01cb902ea5a09d387bafd46a6602a0b914f96b9784e1`  
		Last Modified: Wed, 20 Aug 2025 20:54:06 GMT  
		Size: 207.9 MB (207924648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4dc57f26035f8dc52c2e45dabd6078585da8166099282623161725993e8edd2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3f0e94468d41f8eba6af03807e16bc677a900e68f8429c353832396b7601f3`

```dockerfile
```

-	Layers:
	-	`sha256:f0e9246662234c3fc1435b0f1ba767acc50b73604b03eb13c3cbb642f3b39b99`  
		Last Modified: Wed, 20 Aug 2025 20:53:35 GMT  
		Size: 19.0 KB (18961 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:bb46ce3f842d3e3ad8a72df540071b5f14447a5e23c655d989215d773be460ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215046111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9d30927b42ac20f74ccd8f91ab91d4c3727b6730639befebce1c7f0d144b76`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab492f2b844ab0e6b83f1dc61379567ed6a187423e24cec259e149feb4e4ab7`  
		Last Modified: Wed, 20 Aug 2025 20:54:03 GMT  
		Size: 150.1 MB (150085066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0b86c429573db488866051100a0ee632d741e53055907ab493fc41060f16aad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cfe09089a4f3219c68e4b394b1be7050c1f0d390e7a77b39e69bf84a046622`

```dockerfile
```

-	Layers:
	-	`sha256:4e19f7e18f207d87738b361b1ca6f8302f261685c106c5a6661d8e51c60bfeb9`  
		Last Modified: Wed, 20 Aug 2025 20:53:39 GMT  
		Size: 19.1 KB (19063 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d9e367080af7d7a6a57f2781f4333dbd9005d26f548ebc29fe1450190e10834f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281265106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fadbfae3509bbf907a973d7280590d1150a03a20cb3cab8c369cc9239c3988`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3afea05610d5e523abc7b1b80da95f86be166605de4bc50f647f30021609db`  
		Last Modified: Wed, 20 Aug 2025 18:52:15 GMT  
		Size: 42.3 MB (42265724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6856a5741073f9a038c6f208b8b8c66a087d92e3f8d612594b31b217d6ae444c`  
		Last Modified: Wed, 20 Aug 2025 18:52:11 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24702d5295002e9267969550b7c98f0c74f8875fcae5a97f82eae1fb8e5b650`  
		Last Modified: Wed, 20 Aug 2025 20:54:14 GMT  
		Size: 207.3 MB (207296661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7eeaa1f52aec4062754c686bd18467badb4ec5c00aedc1064875a2e139c209bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05292d6b123362939cc2dd9bfed071412be258ccfdb530ae71e2f4fd0460ce61`

```dockerfile
```

-	Layers:
	-	`sha256:aaeefecd88aeccafb0315f2b0305431275103d192379b42d10e06b20294a3a87`  
		Last Modified: Wed, 20 Aug 2025 20:53:42 GMT  
		Size: 19.1 KB (19095 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:77440ee296dc4830f12f10faadb63b33d70f7e4b5406c9cda9590745e3529ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228193385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43adbe7867b239884bd232412ede9633651568e4a8d55064d322ef4487d4a186`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
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
	-	`sha256:6c021fe7c34d21d36f48e05c739e0f12bb23c30ad7bc32bb246b729ee596cbb5`  
		Last Modified: Fri, 22 Aug 2025 05:53:52 GMT  
		Size: 156.8 MB (156804761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e515ae92445233ad355e5121ec899544ecd520cf711d5c516e2739e03c37f241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d4203225c76bee9800e08281ff6703b7c055fcc90e2009e3ea7140fd0e6648`

```dockerfile
```

-	Layers:
	-	`sha256:43bb18047c17426808937209753c9a0b282b83b12d69727b974166763407691d`  
		Last Modified: Fri, 22 Aug 2025 05:53:30 GMT  
		Size: 19.0 KB (19009 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:43b7d9020d22e9ccaf013a7716e6c20e6da36da2872f70a4d36e025f7344fef5
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
$ docker pull dart@sha256:65060f22a0e187d589b30ffdd4553d994656ccd5bbe3473cd04b6bc9e48da116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295373459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555d91210e04c10028404b6fbb2952b7620b43565ab094abfa19291babd88782`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7611e74feb20851b1130bcc9bd8c0129e7c1c0e3b0020400d2332960f8854d7`  
		Last Modified: Wed, 27 Aug 2025 17:00:12 GMT  
		Size: 42.5 MB (42480136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46a9fcd5ad34d7175be17433da570662d17ffd30c35aff112b4f4b220c54b5d`  
		Last Modified: Wed, 27 Aug 2025 17:00:10 GMT  
		Size: 1.9 MB (1873606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f334ea837b6064ec27edd68df59a7ac0ba0648e73de671ece1a27781d18b6eff`  
		Last Modified: Wed, 27 Aug 2025 17:37:01 GMT  
		Size: 221.2 MB (221246400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:5af6dcf8512465f978cad26efa9eed38dddc3a43adcc73d83d5ed7787a56d428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba575a8886a3bcf3dfaf6c9aecae0032b256afba999424204647c92747f128e2`

```dockerfile
```

-	Layers:
	-	`sha256:281915cdd7a00d4d469d68b2d24d199d7e8cb9bb48527dc7be5fb85737d69729`  
		Last Modified: Wed, 27 Aug 2025 17:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:c0288fc72cdcac166021fdf1845a0df3102d67dc34bed12bac0f31770fa5a191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220750262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9aa78f3e944a684c7b5432a4e8fcbf775188c6004aaaf58f6227192928d6bd8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c057a1b1208d8b91ceb9c549498d8b1070ce4670a3db742f55a508f0e811363`  
		Last Modified: Wed, 27 Aug 2025 17:33:40 GMT  
		Size: 155.8 MB (155789217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:925849d43849db5c4887760f5d39f74cbb4ec1f1dd13dc007ee334095101c4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259ce88380f74e730a0c271ffc31a5cebabaaad844ffa6387e116a8111ea769a`

```dockerfile
```

-	Layers:
	-	`sha256:99f973603e81a94a6610825bc73afb1d7e26eb9bd1e8762fd695ff2322ed2c35`  
		Last Modified: Wed, 27 Aug 2025 17:53:27 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:eae202b79129653e9eba86aa2b7d937dbdee78a9eb6b9798879a76a3c2645868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294654235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffa61f59c0449760929123bb900bc4bfe585d16fbf6892e283f66a5ee30266e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9000d97bea06011816be9f25945ced50f31ad05eb520668404aeb0882fae5609`  
		Last Modified: Wed, 27 Aug 2025 17:00:20 GMT  
		Size: 42.3 MB (42265833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40d1be1d28b90af2e21ab46f813f59af74d9c0dd07026070203719fa487a1c9`  
		Last Modified: Wed, 27 Aug 2025 17:00:17 GMT  
		Size: 1.6 MB (1566651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5358a9be7b571d1319c47f66ddba7723cc565f0ff18de5d8f68742813ba1858d`  
		Last Modified: Wed, 27 Aug 2025 17:42:15 GMT  
		Size: 220.7 MB (220685675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:1f1f1730f412c0133590466bae8974592bc54f999f57a4dae2e86c2c16551a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45157eb41cdb24939321502d589ae9d53558366fe7fd1cd9b330df4bd3c417d`

```dockerfile
```

-	Layers:
	-	`sha256:c221b9c76de5333269e905ad5caa5622b86f9dd4c8fd1d184208873c69f321ec`  
		Last Modified: Wed, 27 Aug 2025 17:53:29 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; riscv64

```console
$ docker pull dart@sha256:f5302601d3823ec52c3b2227298e67a4a71cd07bab4a602a36c3c216af7ccf71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232350305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68799c58a6ba3ad3c460f348bfe1af139662e3b19455eaaadc827b1336c287c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
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
	-	`sha256:6c81a9390d0dea74d0dd5ee5f075ff9d4f75f5b1f488075fc37ae6501f9249d4`  
		Last Modified: Fri, 22 Aug 2025 05:53:45 GMT  
		Size: 161.0 MB (160961681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:b7c8ddd25637b499c8e7236faea5f000cf932d95912f032acf3e6bd18c8c7f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff44dbc8bcdd4e9fd31a3bc8b1291d0abecc7bb011589a4eb5d5eb8e76705e69`

```dockerfile
```

-	Layers:
	-	`sha256:7d474be0622a310b8fc874ca0973e5c9169478864a562a02cbd125139a56f1cb`  
		Last Modified: Fri, 22 Aug 2025 05:53:23 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:43b7d9020d22e9ccaf013a7716e6c20e6da36da2872f70a4d36e025f7344fef5
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
$ docker pull dart@sha256:65060f22a0e187d589b30ffdd4553d994656ccd5bbe3473cd04b6bc9e48da116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295373459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555d91210e04c10028404b6fbb2952b7620b43565ab094abfa19291babd88782`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7611e74feb20851b1130bcc9bd8c0129e7c1c0e3b0020400d2332960f8854d7`  
		Last Modified: Wed, 27 Aug 2025 17:00:12 GMT  
		Size: 42.5 MB (42480136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46a9fcd5ad34d7175be17433da570662d17ffd30c35aff112b4f4b220c54b5d`  
		Last Modified: Wed, 27 Aug 2025 17:00:10 GMT  
		Size: 1.9 MB (1873606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f334ea837b6064ec27edd68df59a7ac0ba0648e73de671ece1a27781d18b6eff`  
		Last Modified: Wed, 27 Aug 2025 17:37:01 GMT  
		Size: 221.2 MB (221246400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5af6dcf8512465f978cad26efa9eed38dddc3a43adcc73d83d5ed7787a56d428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba575a8886a3bcf3dfaf6c9aecae0032b256afba999424204647c92747f128e2`

```dockerfile
```

-	Layers:
	-	`sha256:281915cdd7a00d4d469d68b2d24d199d7e8cb9bb48527dc7be5fb85737d69729`  
		Last Modified: Wed, 27 Aug 2025 17:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:c0288fc72cdcac166021fdf1845a0df3102d67dc34bed12bac0f31770fa5a191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220750262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9aa78f3e944a684c7b5432a4e8fcbf775188c6004aaaf58f6227192928d6bd8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c057a1b1208d8b91ceb9c549498d8b1070ce4670a3db742f55a508f0e811363`  
		Last Modified: Wed, 27 Aug 2025 17:33:40 GMT  
		Size: 155.8 MB (155789217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:925849d43849db5c4887760f5d39f74cbb4ec1f1dd13dc007ee334095101c4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259ce88380f74e730a0c271ffc31a5cebabaaad844ffa6387e116a8111ea769a`

```dockerfile
```

-	Layers:
	-	`sha256:99f973603e81a94a6610825bc73afb1d7e26eb9bd1e8762fd695ff2322ed2c35`  
		Last Modified: Wed, 27 Aug 2025 17:53:27 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:eae202b79129653e9eba86aa2b7d937dbdee78a9eb6b9798879a76a3c2645868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294654235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffa61f59c0449760929123bb900bc4bfe585d16fbf6892e283f66a5ee30266e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9000d97bea06011816be9f25945ced50f31ad05eb520668404aeb0882fae5609`  
		Last Modified: Wed, 27 Aug 2025 17:00:20 GMT  
		Size: 42.3 MB (42265833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40d1be1d28b90af2e21ab46f813f59af74d9c0dd07026070203719fa487a1c9`  
		Last Modified: Wed, 27 Aug 2025 17:00:17 GMT  
		Size: 1.6 MB (1566651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5358a9be7b571d1319c47f66ddba7723cc565f0ff18de5d8f68742813ba1858d`  
		Last Modified: Wed, 27 Aug 2025 17:42:15 GMT  
		Size: 220.7 MB (220685675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1f1f1730f412c0133590466bae8974592bc54f999f57a4dae2e86c2c16551a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45157eb41cdb24939321502d589ae9d53558366fe7fd1cd9b330df4bd3c417d`

```dockerfile
```

-	Layers:
	-	`sha256:c221b9c76de5333269e905ad5caa5622b86f9dd4c8fd1d184208873c69f321ec`  
		Last Modified: Wed, 27 Aug 2025 17:53:29 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; riscv64

```console
$ docker pull dart@sha256:f5302601d3823ec52c3b2227298e67a4a71cd07bab4a602a36c3c216af7ccf71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232350305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68799c58a6ba3ad3c460f348bfe1af139662e3b19455eaaadc827b1336c287c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
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
	-	`sha256:6c81a9390d0dea74d0dd5ee5f075ff9d4f75f5b1f488075fc37ae6501f9249d4`  
		Last Modified: Fri, 22 Aug 2025 05:53:45 GMT  
		Size: 161.0 MB (160961681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b7c8ddd25637b499c8e7236faea5f000cf932d95912f032acf3e6bd18c8c7f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff44dbc8bcdd4e9fd31a3bc8b1291d0abecc7bb011589a4eb5d5eb8e76705e69`

```dockerfile
```

-	Layers:
	-	`sha256:7d474be0622a310b8fc874ca0973e5c9169478864a562a02cbd125139a56f1cb`  
		Last Modified: Fri, 22 Aug 2025 05:53:23 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:43b7d9020d22e9ccaf013a7716e6c20e6da36da2872f70a4d36e025f7344fef5
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
$ docker pull dart@sha256:65060f22a0e187d589b30ffdd4553d994656ccd5bbe3473cd04b6bc9e48da116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295373459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555d91210e04c10028404b6fbb2952b7620b43565ab094abfa19291babd88782`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7611e74feb20851b1130bcc9bd8c0129e7c1c0e3b0020400d2332960f8854d7`  
		Last Modified: Wed, 27 Aug 2025 17:00:12 GMT  
		Size: 42.5 MB (42480136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46a9fcd5ad34d7175be17433da570662d17ffd30c35aff112b4f4b220c54b5d`  
		Last Modified: Wed, 27 Aug 2025 17:00:10 GMT  
		Size: 1.9 MB (1873606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f334ea837b6064ec27edd68df59a7ac0ba0648e73de671ece1a27781d18b6eff`  
		Last Modified: Wed, 27 Aug 2025 17:37:01 GMT  
		Size: 221.2 MB (221246400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:5af6dcf8512465f978cad26efa9eed38dddc3a43adcc73d83d5ed7787a56d428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba575a8886a3bcf3dfaf6c9aecae0032b256afba999424204647c92747f128e2`

```dockerfile
```

-	Layers:
	-	`sha256:281915cdd7a00d4d469d68b2d24d199d7e8cb9bb48527dc7be5fb85737d69729`  
		Last Modified: Wed, 27 Aug 2025 17:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:c0288fc72cdcac166021fdf1845a0df3102d67dc34bed12bac0f31770fa5a191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220750262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9aa78f3e944a684c7b5432a4e8fcbf775188c6004aaaf58f6227192928d6bd8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c057a1b1208d8b91ceb9c549498d8b1070ce4670a3db742f55a508f0e811363`  
		Last Modified: Wed, 27 Aug 2025 17:33:40 GMT  
		Size: 155.8 MB (155789217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:925849d43849db5c4887760f5d39f74cbb4ec1f1dd13dc007ee334095101c4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259ce88380f74e730a0c271ffc31a5cebabaaad844ffa6387e116a8111ea769a`

```dockerfile
```

-	Layers:
	-	`sha256:99f973603e81a94a6610825bc73afb1d7e26eb9bd1e8762fd695ff2322ed2c35`  
		Last Modified: Wed, 27 Aug 2025 17:53:27 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:eae202b79129653e9eba86aa2b7d937dbdee78a9eb6b9798879a76a3c2645868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294654235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffa61f59c0449760929123bb900bc4bfe585d16fbf6892e283f66a5ee30266e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9000d97bea06011816be9f25945ced50f31ad05eb520668404aeb0882fae5609`  
		Last Modified: Wed, 27 Aug 2025 17:00:20 GMT  
		Size: 42.3 MB (42265833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40d1be1d28b90af2e21ab46f813f59af74d9c0dd07026070203719fa487a1c9`  
		Last Modified: Wed, 27 Aug 2025 17:00:17 GMT  
		Size: 1.6 MB (1566651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5358a9be7b571d1319c47f66ddba7723cc565f0ff18de5d8f68742813ba1858d`  
		Last Modified: Wed, 27 Aug 2025 17:42:15 GMT  
		Size: 220.7 MB (220685675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:1f1f1730f412c0133590466bae8974592bc54f999f57a4dae2e86c2c16551a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45157eb41cdb24939321502d589ae9d53558366fe7fd1cd9b330df4bd3c417d`

```dockerfile
```

-	Layers:
	-	`sha256:c221b9c76de5333269e905ad5caa5622b86f9dd4c8fd1d184208873c69f321ec`  
		Last Modified: Wed, 27 Aug 2025 17:53:29 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; riscv64

```console
$ docker pull dart@sha256:f5302601d3823ec52c3b2227298e67a4a71cd07bab4a602a36c3c216af7ccf71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232350305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68799c58a6ba3ad3c460f348bfe1af139662e3b19455eaaadc827b1336c287c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
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
	-	`sha256:6c81a9390d0dea74d0dd5ee5f075ff9d4f75f5b1f488075fc37ae6501f9249d4`  
		Last Modified: Fri, 22 Aug 2025 05:53:45 GMT  
		Size: 161.0 MB (160961681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:b7c8ddd25637b499c8e7236faea5f000cf932d95912f032acf3e6bd18c8c7f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff44dbc8bcdd4e9fd31a3bc8b1291d0abecc7bb011589a4eb5d5eb8e76705e69`

```dockerfile
```

-	Layers:
	-	`sha256:7d474be0622a310b8fc874ca0973e5c9169478864a562a02cbd125139a56f1cb`  
		Last Modified: Fri, 22 Aug 2025 05:53:23 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:43b7d9020d22e9ccaf013a7716e6c20e6da36da2872f70a4d36e025f7344fef5
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
$ docker pull dart@sha256:65060f22a0e187d589b30ffdd4553d994656ccd5bbe3473cd04b6bc9e48da116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295373459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555d91210e04c10028404b6fbb2952b7620b43565ab094abfa19291babd88782`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7611e74feb20851b1130bcc9bd8c0129e7c1c0e3b0020400d2332960f8854d7`  
		Last Modified: Wed, 27 Aug 2025 17:00:12 GMT  
		Size: 42.5 MB (42480136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46a9fcd5ad34d7175be17433da570662d17ffd30c35aff112b4f4b220c54b5d`  
		Last Modified: Wed, 27 Aug 2025 17:00:10 GMT  
		Size: 1.9 MB (1873606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f334ea837b6064ec27edd68df59a7ac0ba0648e73de671ece1a27781d18b6eff`  
		Last Modified: Wed, 27 Aug 2025 17:37:01 GMT  
		Size: 221.2 MB (221246400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5af6dcf8512465f978cad26efa9eed38dddc3a43adcc73d83d5ed7787a56d428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba575a8886a3bcf3dfaf6c9aecae0032b256afba999424204647c92747f128e2`

```dockerfile
```

-	Layers:
	-	`sha256:281915cdd7a00d4d469d68b2d24d199d7e8cb9bb48527dc7be5fb85737d69729`  
		Last Modified: Wed, 27 Aug 2025 17:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:c0288fc72cdcac166021fdf1845a0df3102d67dc34bed12bac0f31770fa5a191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220750262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9aa78f3e944a684c7b5432a4e8fcbf775188c6004aaaf58f6227192928d6bd8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c057a1b1208d8b91ceb9c549498d8b1070ce4670a3db742f55a508f0e811363`  
		Last Modified: Wed, 27 Aug 2025 17:33:40 GMT  
		Size: 155.8 MB (155789217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:925849d43849db5c4887760f5d39f74cbb4ec1f1dd13dc007ee334095101c4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259ce88380f74e730a0c271ffc31a5cebabaaad844ffa6387e116a8111ea769a`

```dockerfile
```

-	Layers:
	-	`sha256:99f973603e81a94a6610825bc73afb1d7e26eb9bd1e8762fd695ff2322ed2c35`  
		Last Modified: Wed, 27 Aug 2025 17:53:27 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:eae202b79129653e9eba86aa2b7d937dbdee78a9eb6b9798879a76a3c2645868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294654235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffa61f59c0449760929123bb900bc4bfe585d16fbf6892e283f66a5ee30266e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9000d97bea06011816be9f25945ced50f31ad05eb520668404aeb0882fae5609`  
		Last Modified: Wed, 27 Aug 2025 17:00:20 GMT  
		Size: 42.3 MB (42265833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40d1be1d28b90af2e21ab46f813f59af74d9c0dd07026070203719fa487a1c9`  
		Last Modified: Wed, 27 Aug 2025 17:00:17 GMT  
		Size: 1.6 MB (1566651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5358a9be7b571d1319c47f66ddba7723cc565f0ff18de5d8f68742813ba1858d`  
		Last Modified: Wed, 27 Aug 2025 17:42:15 GMT  
		Size: 220.7 MB (220685675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1f1f1730f412c0133590466bae8974592bc54f999f57a4dae2e86c2c16551a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45157eb41cdb24939321502d589ae9d53558366fe7fd1cd9b330df4bd3c417d`

```dockerfile
```

-	Layers:
	-	`sha256:c221b9c76de5333269e905ad5caa5622b86f9dd4c8fd1d184208873c69f321ec`  
		Last Modified: Wed, 27 Aug 2025 17:53:29 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:f5302601d3823ec52c3b2227298e67a4a71cd07bab4a602a36c3c216af7ccf71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232350305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68799c58a6ba3ad3c460f348bfe1af139662e3b19455eaaadc827b1336c287c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
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
	-	`sha256:6c81a9390d0dea74d0dd5ee5f075ff9d4f75f5b1f488075fc37ae6501f9249d4`  
		Last Modified: Fri, 22 Aug 2025 05:53:45 GMT  
		Size: 161.0 MB (160961681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b7c8ddd25637b499c8e7236faea5f000cf932d95912f032acf3e6bd18c8c7f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff44dbc8bcdd4e9fd31a3bc8b1291d0abecc7bb011589a4eb5d5eb8e76705e69`

```dockerfile
```

-	Layers:
	-	`sha256:7d474be0622a310b8fc874ca0973e5c9169478864a562a02cbd125139a56f1cb`  
		Last Modified: Fri, 22 Aug 2025 05:53:23 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json
