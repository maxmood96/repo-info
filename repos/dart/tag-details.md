<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.11`](#dart311)
-	[`dart:3.11-sdk`](#dart311-sdk)
-	[`dart:3.11.2`](#dart3112)
-	[`dart:3.11.2-sdk`](#dart3112-sdk)
-	[`dart:3.12.0-210.1.beta`](#dart3120-2101beta)
-	[`dart:3.12.0-210.1.beta-sdk`](#dart3120-2101beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:318d267b31b9fc3cd86420785fab5c493084b5d3dd16dc6159731ec93f10a2ba
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
$ docker pull dart@sha256:0f14c3efce955560a7fdfdca6255ba28fca2dbaa823164385345f8a3aa393053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307068588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd480997ad8dfd9ce83532e18af4fb7f1e571dd92a0d479a7201fdcbbdccc4f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:39:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:39:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:39:59 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:40:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b983e8e71d710fa468d653755314ad0ee7f22241ca986012be178cdce4cb6e`  
		Last Modified: Mon, 16 Mar 2026 22:40:37 GMT  
		Size: 42.5 MB (42491632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e163ed7ccec9c4b4953f644d92db0169ce321a174454a0d9bd26dab1b5e59c3`  
		Last Modified: Mon, 16 Mar 2026 22:40:35 GMT  
		Size: 1.9 MB (1869562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fd2d4c728cf7bbb085d8d05545eb5528550bf00e14b1d65c8593700384d518`  
		Last Modified: Mon, 16 Mar 2026 22:40:40 GMT  
		Size: 232.9 MB (232931862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:e5fed519048230aca05cd25a3511419592f9d2a5d17bd363f7842b45bc567d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332f9ba42d7cf4c4d901003935431ba1fff95df2e17fac09cdaa63e589912bff`

```dockerfile
```

-	Layers:
	-	`sha256:2c50f5fce5f35cb9ef7e2a28701d95ccb2672d1ddd113cf55e8ff2d0db984016`  
		Last Modified: Mon, 16 Mar 2026 22:40:35 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:4ca8dfc4e10a96b4add5a23e3183aa235c7164e7808063cdeda111f5fd590d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222899348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc2a12b194affa14cdd93476accc96a38c7377a0648d0307a456ae5eac7e36d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:24:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 23:24:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:24:51 GMT
WORKDIR /root
# Mon, 16 Mar 2026 23:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3259b2a1aba5d57e776bc237db3cff79430c80aee94c20a667b063739d161ac9`  
		Last Modified: Mon, 16 Mar 2026 23:25:19 GMT  
		Size: 37.5 MB (37494794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702c1366fd82e973caa542275d0ea83ce3db61fb029842b4a4a65214db82c2d`  
		Last Modified: Mon, 16 Mar 2026 23:25:18 GMT  
		Size: 1.3 MB (1273164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53e6767f19d52512c72d601e689e99b7f93abc3d33625db81c86f146967b4f5`  
		Last Modified: Mon, 16 Mar 2026 23:25:21 GMT  
		Size: 157.9 MB (157921853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:1c0eb28090db31a667732c21e7a5bd7c96d549d60820730d88e25141929c6b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bffbae0171b2ccf3dd57244ed7a66bc3c95b38cd8ae6ab6c8fb355a212e05be`

```dockerfile
```

-	Layers:
	-	`sha256:386cd7fe0a8644f0b603c687a1aa5598bd6e769402ac6db61ac4089cf419be11`  
		Last Modified: Mon, 16 Mar 2026 23:25:18 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:452d4b44d161dab6cd084bf64c9e57b6a72ed544f9c87b234e3b91583d5c2eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305429760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c7baeb387236b518cb2eebf21cbb60825683085c0c901b8e8a7cbb5e3ed250`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:42:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:42:24 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:42:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:42:24 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:42:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e9cd5e64802379c3eca7f4180704606eef04f0ed0ae6be113d248a71a91433`  
		Last Modified: Mon, 16 Mar 2026 22:43:04 GMT  
		Size: 42.3 MB (42291389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939ba89df0d01d7eb5da514d268117c5dfeb74882a2d15f951e375ee457e3ef1`  
		Last Modified: Mon, 16 Mar 2026 22:43:02 GMT  
		Size: 1.6 MB (1564356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3739a474ab9a11da8519ece2334e297dce18837220bf00b21eb088688f541b38`  
		Last Modified: Mon, 16 Mar 2026 22:43:07 GMT  
		Size: 231.4 MB (231435567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:f4e8e5e09bdd5f0f84f6567fc2a63f9eb61c8c6ce2c4a34b01c1bfc196bcd8d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34fbe6569738d95356edebe24c3cd07771984fc5f28a7557fff9738352be91c`

```dockerfile
```

-	Layers:
	-	`sha256:b8115bfec7c27f309fb104e42465ad44e5d317aaddf25186f128eda616ef8e2d`  
		Last Modified: Mon, 16 Mar 2026 22:43:02 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; riscv64

```console
$ docker pull dart@sha256:042f25b2cc5fdf8e71de6bc15fc1c8098e1dfc2831d78647fda0eb971d8e8c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a48f0a5a679b127ba6438717506cc63e6af2971961ded82da8b5e3d06c5f20d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 05:45:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Mar 2026 05:45:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Mar 2026 05:45:57 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Mar 2026 05:45:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 05:45:57 GMT
WORKDIR /root
# Wed, 11 Mar 2026 05:46:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0891e80814e4c6f8ac7b39a3234a0ed05f01c28ceb68a7414e7253dd49b5574`  
		Last Modified: Wed, 11 Mar 2026 05:51:07 GMT  
		Size: 41.6 MB (41560567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c677769d0438169b5a3d2ea190fd01a6f426789e4d1b44ac567c6fd4199ae7bd`  
		Last Modified: Wed, 11 Mar 2026 05:50:56 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39319aecdf44b1db93065cd12615111cf7735effea6e530a342c3da06cf9897d`  
		Last Modified: Wed, 11 Mar 2026 05:51:28 GMT  
		Size: 180.5 MB (180483788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:36136486b8b169fbe029a4765b424489acb2b4155a666f71dc4e4e82205e1e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd29552cd62ba524024d08385005f46367f6888fe656c0725c3aceefcaa23fe3`

```dockerfile
```

-	Layers:
	-	`sha256:1ac0fb2033730e2430e102f90ba756922f5a29618328ce1fd38dacb64e1a9dcb`  
		Last Modified: Wed, 11 Mar 2026 05:50:55 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:318d267b31b9fc3cd86420785fab5c493084b5d3dd16dc6159731ec93f10a2ba
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
$ docker pull dart@sha256:0f14c3efce955560a7fdfdca6255ba28fca2dbaa823164385345f8a3aa393053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307068588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd480997ad8dfd9ce83532e18af4fb7f1e571dd92a0d479a7201fdcbbdccc4f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:39:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:39:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:39:59 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:40:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b983e8e71d710fa468d653755314ad0ee7f22241ca986012be178cdce4cb6e`  
		Last Modified: Mon, 16 Mar 2026 22:40:37 GMT  
		Size: 42.5 MB (42491632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e163ed7ccec9c4b4953f644d92db0169ce321a174454a0d9bd26dab1b5e59c3`  
		Last Modified: Mon, 16 Mar 2026 22:40:35 GMT  
		Size: 1.9 MB (1869562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fd2d4c728cf7bbb085d8d05545eb5528550bf00e14b1d65c8593700384d518`  
		Last Modified: Mon, 16 Mar 2026 22:40:40 GMT  
		Size: 232.9 MB (232931862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e5fed519048230aca05cd25a3511419592f9d2a5d17bd363f7842b45bc567d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332f9ba42d7cf4c4d901003935431ba1fff95df2e17fac09cdaa63e589912bff`

```dockerfile
```

-	Layers:
	-	`sha256:2c50f5fce5f35cb9ef7e2a28701d95ccb2672d1ddd113cf55e8ff2d0db984016`  
		Last Modified: Mon, 16 Mar 2026 22:40:35 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:4ca8dfc4e10a96b4add5a23e3183aa235c7164e7808063cdeda111f5fd590d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222899348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc2a12b194affa14cdd93476accc96a38c7377a0648d0307a456ae5eac7e36d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:24:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 23:24:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:24:51 GMT
WORKDIR /root
# Mon, 16 Mar 2026 23:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3259b2a1aba5d57e776bc237db3cff79430c80aee94c20a667b063739d161ac9`  
		Last Modified: Mon, 16 Mar 2026 23:25:19 GMT  
		Size: 37.5 MB (37494794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702c1366fd82e973caa542275d0ea83ce3db61fb029842b4a4a65214db82c2d`  
		Last Modified: Mon, 16 Mar 2026 23:25:18 GMT  
		Size: 1.3 MB (1273164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53e6767f19d52512c72d601e689e99b7f93abc3d33625db81c86f146967b4f5`  
		Last Modified: Mon, 16 Mar 2026 23:25:21 GMT  
		Size: 157.9 MB (157921853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1c0eb28090db31a667732c21e7a5bd7c96d549d60820730d88e25141929c6b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bffbae0171b2ccf3dd57244ed7a66bc3c95b38cd8ae6ab6c8fb355a212e05be`

```dockerfile
```

-	Layers:
	-	`sha256:386cd7fe0a8644f0b603c687a1aa5598bd6e769402ac6db61ac4089cf419be11`  
		Last Modified: Mon, 16 Mar 2026 23:25:18 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:452d4b44d161dab6cd084bf64c9e57b6a72ed544f9c87b234e3b91583d5c2eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305429760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c7baeb387236b518cb2eebf21cbb60825683085c0c901b8e8a7cbb5e3ed250`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:42:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:42:24 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:42:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:42:24 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:42:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e9cd5e64802379c3eca7f4180704606eef04f0ed0ae6be113d248a71a91433`  
		Last Modified: Mon, 16 Mar 2026 22:43:04 GMT  
		Size: 42.3 MB (42291389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939ba89df0d01d7eb5da514d268117c5dfeb74882a2d15f951e375ee457e3ef1`  
		Last Modified: Mon, 16 Mar 2026 22:43:02 GMT  
		Size: 1.6 MB (1564356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3739a474ab9a11da8519ece2334e297dce18837220bf00b21eb088688f541b38`  
		Last Modified: Mon, 16 Mar 2026 22:43:07 GMT  
		Size: 231.4 MB (231435567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:f4e8e5e09bdd5f0f84f6567fc2a63f9eb61c8c6ce2c4a34b01c1bfc196bcd8d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34fbe6569738d95356edebe24c3cd07771984fc5f28a7557fff9738352be91c`

```dockerfile
```

-	Layers:
	-	`sha256:b8115bfec7c27f309fb104e42465ad44e5d317aaddf25186f128eda616ef8e2d`  
		Last Modified: Mon, 16 Mar 2026 22:43:02 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:042f25b2cc5fdf8e71de6bc15fc1c8098e1dfc2831d78647fda0eb971d8e8c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a48f0a5a679b127ba6438717506cc63e6af2971961ded82da8b5e3d06c5f20d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 05:45:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Mar 2026 05:45:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Mar 2026 05:45:57 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Mar 2026 05:45:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 05:45:57 GMT
WORKDIR /root
# Wed, 11 Mar 2026 05:46:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0891e80814e4c6f8ac7b39a3234a0ed05f01c28ceb68a7414e7253dd49b5574`  
		Last Modified: Wed, 11 Mar 2026 05:51:07 GMT  
		Size: 41.6 MB (41560567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c677769d0438169b5a3d2ea190fd01a6f426789e4d1b44ac567c6fd4199ae7bd`  
		Last Modified: Wed, 11 Mar 2026 05:50:56 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39319aecdf44b1db93065cd12615111cf7735effea6e530a342c3da06cf9897d`  
		Last Modified: Wed, 11 Mar 2026 05:51:28 GMT  
		Size: 180.5 MB (180483788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:36136486b8b169fbe029a4765b424489acb2b4155a666f71dc4e4e82205e1e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd29552cd62ba524024d08385005f46367f6888fe656c0725c3aceefcaa23fe3`

```dockerfile
```

-	Layers:
	-	`sha256:1ac0fb2033730e2430e102f90ba756922f5a29618328ce1fd38dacb64e1a9dcb`  
		Last Modified: Wed, 11 Mar 2026 05:50:55 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11`

```console
$ docker pull dart@sha256:318d267b31b9fc3cd86420785fab5c493084b5d3dd16dc6159731ec93f10a2ba
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
$ docker pull dart@sha256:0f14c3efce955560a7fdfdca6255ba28fca2dbaa823164385345f8a3aa393053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307068588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd480997ad8dfd9ce83532e18af4fb7f1e571dd92a0d479a7201fdcbbdccc4f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:39:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:39:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:39:59 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:40:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b983e8e71d710fa468d653755314ad0ee7f22241ca986012be178cdce4cb6e`  
		Last Modified: Mon, 16 Mar 2026 22:40:37 GMT  
		Size: 42.5 MB (42491632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e163ed7ccec9c4b4953f644d92db0169ce321a174454a0d9bd26dab1b5e59c3`  
		Last Modified: Mon, 16 Mar 2026 22:40:35 GMT  
		Size: 1.9 MB (1869562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fd2d4c728cf7bbb085d8d05545eb5528550bf00e14b1d65c8593700384d518`  
		Last Modified: Mon, 16 Mar 2026 22:40:40 GMT  
		Size: 232.9 MB (232931862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:e5fed519048230aca05cd25a3511419592f9d2a5d17bd363f7842b45bc567d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332f9ba42d7cf4c4d901003935431ba1fff95df2e17fac09cdaa63e589912bff`

```dockerfile
```

-	Layers:
	-	`sha256:2c50f5fce5f35cb9ef7e2a28701d95ccb2672d1ddd113cf55e8ff2d0db984016`  
		Last Modified: Mon, 16 Mar 2026 22:40:35 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11` - linux; arm variant v7

```console
$ docker pull dart@sha256:4ca8dfc4e10a96b4add5a23e3183aa235c7164e7808063cdeda111f5fd590d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222899348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc2a12b194affa14cdd93476accc96a38c7377a0648d0307a456ae5eac7e36d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:24:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 23:24:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:24:51 GMT
WORKDIR /root
# Mon, 16 Mar 2026 23:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3259b2a1aba5d57e776bc237db3cff79430c80aee94c20a667b063739d161ac9`  
		Last Modified: Mon, 16 Mar 2026 23:25:19 GMT  
		Size: 37.5 MB (37494794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702c1366fd82e973caa542275d0ea83ce3db61fb029842b4a4a65214db82c2d`  
		Last Modified: Mon, 16 Mar 2026 23:25:18 GMT  
		Size: 1.3 MB (1273164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53e6767f19d52512c72d601e689e99b7f93abc3d33625db81c86f146967b4f5`  
		Last Modified: Mon, 16 Mar 2026 23:25:21 GMT  
		Size: 157.9 MB (157921853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:1c0eb28090db31a667732c21e7a5bd7c96d549d60820730d88e25141929c6b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bffbae0171b2ccf3dd57244ed7a66bc3c95b38cd8ae6ab6c8fb355a212e05be`

```dockerfile
```

-	Layers:
	-	`sha256:386cd7fe0a8644f0b603c687a1aa5598bd6e769402ac6db61ac4089cf419be11`  
		Last Modified: Mon, 16 Mar 2026 23:25:18 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:452d4b44d161dab6cd084bf64c9e57b6a72ed544f9c87b234e3b91583d5c2eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305429760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c7baeb387236b518cb2eebf21cbb60825683085c0c901b8e8a7cbb5e3ed250`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:42:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:42:24 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:42:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:42:24 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:42:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e9cd5e64802379c3eca7f4180704606eef04f0ed0ae6be113d248a71a91433`  
		Last Modified: Mon, 16 Mar 2026 22:43:04 GMT  
		Size: 42.3 MB (42291389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939ba89df0d01d7eb5da514d268117c5dfeb74882a2d15f951e375ee457e3ef1`  
		Last Modified: Mon, 16 Mar 2026 22:43:02 GMT  
		Size: 1.6 MB (1564356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3739a474ab9a11da8519ece2334e297dce18837220bf00b21eb088688f541b38`  
		Last Modified: Mon, 16 Mar 2026 22:43:07 GMT  
		Size: 231.4 MB (231435567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:f4e8e5e09bdd5f0f84f6567fc2a63f9eb61c8c6ce2c4a34b01c1bfc196bcd8d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34fbe6569738d95356edebe24c3cd07771984fc5f28a7557fff9738352be91c`

```dockerfile
```

-	Layers:
	-	`sha256:b8115bfec7c27f309fb104e42465ad44e5d317aaddf25186f128eda616ef8e2d`  
		Last Modified: Mon, 16 Mar 2026 22:43:02 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11` - linux; riscv64

```console
$ docker pull dart@sha256:042f25b2cc5fdf8e71de6bc15fc1c8098e1dfc2831d78647fda0eb971d8e8c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a48f0a5a679b127ba6438717506cc63e6af2971961ded82da8b5e3d06c5f20d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 05:45:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Mar 2026 05:45:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Mar 2026 05:45:57 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Mar 2026 05:45:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 05:45:57 GMT
WORKDIR /root
# Wed, 11 Mar 2026 05:46:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0891e80814e4c6f8ac7b39a3234a0ed05f01c28ceb68a7414e7253dd49b5574`  
		Last Modified: Wed, 11 Mar 2026 05:51:07 GMT  
		Size: 41.6 MB (41560567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c677769d0438169b5a3d2ea190fd01a6f426789e4d1b44ac567c6fd4199ae7bd`  
		Last Modified: Wed, 11 Mar 2026 05:50:56 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39319aecdf44b1db93065cd12615111cf7735effea6e530a342c3da06cf9897d`  
		Last Modified: Wed, 11 Mar 2026 05:51:28 GMT  
		Size: 180.5 MB (180483788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:36136486b8b169fbe029a4765b424489acb2b4155a666f71dc4e4e82205e1e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd29552cd62ba524024d08385005f46367f6888fe656c0725c3aceefcaa23fe3`

```dockerfile
```

-	Layers:
	-	`sha256:1ac0fb2033730e2430e102f90ba756922f5a29618328ce1fd38dacb64e1a9dcb`  
		Last Modified: Wed, 11 Mar 2026 05:50:55 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11-sdk`

```console
$ docker pull dart@sha256:318d267b31b9fc3cd86420785fab5c493084b5d3dd16dc6159731ec93f10a2ba
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
$ docker pull dart@sha256:0f14c3efce955560a7fdfdca6255ba28fca2dbaa823164385345f8a3aa393053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307068588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd480997ad8dfd9ce83532e18af4fb7f1e571dd92a0d479a7201fdcbbdccc4f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:39:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:39:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:39:59 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:40:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b983e8e71d710fa468d653755314ad0ee7f22241ca986012be178cdce4cb6e`  
		Last Modified: Mon, 16 Mar 2026 22:40:37 GMT  
		Size: 42.5 MB (42491632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e163ed7ccec9c4b4953f644d92db0169ce321a174454a0d9bd26dab1b5e59c3`  
		Last Modified: Mon, 16 Mar 2026 22:40:35 GMT  
		Size: 1.9 MB (1869562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fd2d4c728cf7bbb085d8d05545eb5528550bf00e14b1d65c8593700384d518`  
		Last Modified: Mon, 16 Mar 2026 22:40:40 GMT  
		Size: 232.9 MB (232931862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e5fed519048230aca05cd25a3511419592f9d2a5d17bd363f7842b45bc567d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332f9ba42d7cf4c4d901003935431ba1fff95df2e17fac09cdaa63e589912bff`

```dockerfile
```

-	Layers:
	-	`sha256:2c50f5fce5f35cb9ef7e2a28701d95ccb2672d1ddd113cf55e8ff2d0db984016`  
		Last Modified: Mon, 16 Mar 2026 22:40:35 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:4ca8dfc4e10a96b4add5a23e3183aa235c7164e7808063cdeda111f5fd590d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222899348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc2a12b194affa14cdd93476accc96a38c7377a0648d0307a456ae5eac7e36d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:24:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 23:24:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:24:51 GMT
WORKDIR /root
# Mon, 16 Mar 2026 23:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3259b2a1aba5d57e776bc237db3cff79430c80aee94c20a667b063739d161ac9`  
		Last Modified: Mon, 16 Mar 2026 23:25:19 GMT  
		Size: 37.5 MB (37494794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702c1366fd82e973caa542275d0ea83ce3db61fb029842b4a4a65214db82c2d`  
		Last Modified: Mon, 16 Mar 2026 23:25:18 GMT  
		Size: 1.3 MB (1273164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53e6767f19d52512c72d601e689e99b7f93abc3d33625db81c86f146967b4f5`  
		Last Modified: Mon, 16 Mar 2026 23:25:21 GMT  
		Size: 157.9 MB (157921853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1c0eb28090db31a667732c21e7a5bd7c96d549d60820730d88e25141929c6b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bffbae0171b2ccf3dd57244ed7a66bc3c95b38cd8ae6ab6c8fb355a212e05be`

```dockerfile
```

-	Layers:
	-	`sha256:386cd7fe0a8644f0b603c687a1aa5598bd6e769402ac6db61ac4089cf419be11`  
		Last Modified: Mon, 16 Mar 2026 23:25:18 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:452d4b44d161dab6cd084bf64c9e57b6a72ed544f9c87b234e3b91583d5c2eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305429760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c7baeb387236b518cb2eebf21cbb60825683085c0c901b8e8a7cbb5e3ed250`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:42:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:42:24 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:42:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:42:24 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:42:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e9cd5e64802379c3eca7f4180704606eef04f0ed0ae6be113d248a71a91433`  
		Last Modified: Mon, 16 Mar 2026 22:43:04 GMT  
		Size: 42.3 MB (42291389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939ba89df0d01d7eb5da514d268117c5dfeb74882a2d15f951e375ee457e3ef1`  
		Last Modified: Mon, 16 Mar 2026 22:43:02 GMT  
		Size: 1.6 MB (1564356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3739a474ab9a11da8519ece2334e297dce18837220bf00b21eb088688f541b38`  
		Last Modified: Mon, 16 Mar 2026 22:43:07 GMT  
		Size: 231.4 MB (231435567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:f4e8e5e09bdd5f0f84f6567fc2a63f9eb61c8c6ce2c4a34b01c1bfc196bcd8d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34fbe6569738d95356edebe24c3cd07771984fc5f28a7557fff9738352be91c`

```dockerfile
```

-	Layers:
	-	`sha256:b8115bfec7c27f309fb104e42465ad44e5d317aaddf25186f128eda616ef8e2d`  
		Last Modified: Mon, 16 Mar 2026 22:43:02 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:042f25b2cc5fdf8e71de6bc15fc1c8098e1dfc2831d78647fda0eb971d8e8c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a48f0a5a679b127ba6438717506cc63e6af2971961ded82da8b5e3d06c5f20d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 05:45:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Mar 2026 05:45:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Mar 2026 05:45:57 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Mar 2026 05:45:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 05:45:57 GMT
WORKDIR /root
# Wed, 11 Mar 2026 05:46:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0891e80814e4c6f8ac7b39a3234a0ed05f01c28ceb68a7414e7253dd49b5574`  
		Last Modified: Wed, 11 Mar 2026 05:51:07 GMT  
		Size: 41.6 MB (41560567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c677769d0438169b5a3d2ea190fd01a6f426789e4d1b44ac567c6fd4199ae7bd`  
		Last Modified: Wed, 11 Mar 2026 05:50:56 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39319aecdf44b1db93065cd12615111cf7735effea6e530a342c3da06cf9897d`  
		Last Modified: Wed, 11 Mar 2026 05:51:28 GMT  
		Size: 180.5 MB (180483788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:36136486b8b169fbe029a4765b424489acb2b4155a666f71dc4e4e82205e1e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd29552cd62ba524024d08385005f46367f6888fe656c0725c3aceefcaa23fe3`

```dockerfile
```

-	Layers:
	-	`sha256:1ac0fb2033730e2430e102f90ba756922f5a29618328ce1fd38dacb64e1a9dcb`  
		Last Modified: Wed, 11 Mar 2026 05:50:55 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.2`

```console
$ docker pull dart@sha256:318d267b31b9fc3cd86420785fab5c493084b5d3dd16dc6159731ec93f10a2ba
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

### `dart:3.11.2` - linux; amd64

```console
$ docker pull dart@sha256:0f14c3efce955560a7fdfdca6255ba28fca2dbaa823164385345f8a3aa393053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307068588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd480997ad8dfd9ce83532e18af4fb7f1e571dd92a0d479a7201fdcbbdccc4f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:39:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:39:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:39:59 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:40:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b983e8e71d710fa468d653755314ad0ee7f22241ca986012be178cdce4cb6e`  
		Last Modified: Mon, 16 Mar 2026 22:40:37 GMT  
		Size: 42.5 MB (42491632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e163ed7ccec9c4b4953f644d92db0169ce321a174454a0d9bd26dab1b5e59c3`  
		Last Modified: Mon, 16 Mar 2026 22:40:35 GMT  
		Size: 1.9 MB (1869562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fd2d4c728cf7bbb085d8d05545eb5528550bf00e14b1d65c8593700384d518`  
		Last Modified: Mon, 16 Mar 2026 22:40:40 GMT  
		Size: 232.9 MB (232931862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.2` - unknown; unknown

```console
$ docker pull dart@sha256:e5fed519048230aca05cd25a3511419592f9d2a5d17bd363f7842b45bc567d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332f9ba42d7cf4c4d901003935431ba1fff95df2e17fac09cdaa63e589912bff`

```dockerfile
```

-	Layers:
	-	`sha256:2c50f5fce5f35cb9ef7e2a28701d95ccb2672d1ddd113cf55e8ff2d0db984016`  
		Last Modified: Mon, 16 Mar 2026 22:40:35 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.2` - linux; arm variant v7

```console
$ docker pull dart@sha256:4ca8dfc4e10a96b4add5a23e3183aa235c7164e7808063cdeda111f5fd590d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222899348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc2a12b194affa14cdd93476accc96a38c7377a0648d0307a456ae5eac7e36d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:24:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 23:24:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:24:51 GMT
WORKDIR /root
# Mon, 16 Mar 2026 23:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3259b2a1aba5d57e776bc237db3cff79430c80aee94c20a667b063739d161ac9`  
		Last Modified: Mon, 16 Mar 2026 23:25:19 GMT  
		Size: 37.5 MB (37494794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702c1366fd82e973caa542275d0ea83ce3db61fb029842b4a4a65214db82c2d`  
		Last Modified: Mon, 16 Mar 2026 23:25:18 GMT  
		Size: 1.3 MB (1273164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53e6767f19d52512c72d601e689e99b7f93abc3d33625db81c86f146967b4f5`  
		Last Modified: Mon, 16 Mar 2026 23:25:21 GMT  
		Size: 157.9 MB (157921853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.2` - unknown; unknown

```console
$ docker pull dart@sha256:1c0eb28090db31a667732c21e7a5bd7c96d549d60820730d88e25141929c6b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bffbae0171b2ccf3dd57244ed7a66bc3c95b38cd8ae6ab6c8fb355a212e05be`

```dockerfile
```

-	Layers:
	-	`sha256:386cd7fe0a8644f0b603c687a1aa5598bd6e769402ac6db61ac4089cf419be11`  
		Last Modified: Mon, 16 Mar 2026 23:25:18 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.2` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:452d4b44d161dab6cd084bf64c9e57b6a72ed544f9c87b234e3b91583d5c2eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305429760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c7baeb387236b518cb2eebf21cbb60825683085c0c901b8e8a7cbb5e3ed250`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:42:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:42:24 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:42:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:42:24 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:42:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e9cd5e64802379c3eca7f4180704606eef04f0ed0ae6be113d248a71a91433`  
		Last Modified: Mon, 16 Mar 2026 22:43:04 GMT  
		Size: 42.3 MB (42291389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939ba89df0d01d7eb5da514d268117c5dfeb74882a2d15f951e375ee457e3ef1`  
		Last Modified: Mon, 16 Mar 2026 22:43:02 GMT  
		Size: 1.6 MB (1564356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3739a474ab9a11da8519ece2334e297dce18837220bf00b21eb088688f541b38`  
		Last Modified: Mon, 16 Mar 2026 22:43:07 GMT  
		Size: 231.4 MB (231435567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.2` - unknown; unknown

```console
$ docker pull dart@sha256:f4e8e5e09bdd5f0f84f6567fc2a63f9eb61c8c6ce2c4a34b01c1bfc196bcd8d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34fbe6569738d95356edebe24c3cd07771984fc5f28a7557fff9738352be91c`

```dockerfile
```

-	Layers:
	-	`sha256:b8115bfec7c27f309fb104e42465ad44e5d317aaddf25186f128eda616ef8e2d`  
		Last Modified: Mon, 16 Mar 2026 22:43:02 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.2` - linux; riscv64

```console
$ docker pull dart@sha256:042f25b2cc5fdf8e71de6bc15fc1c8098e1dfc2831d78647fda0eb971d8e8c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a48f0a5a679b127ba6438717506cc63e6af2971961ded82da8b5e3d06c5f20d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 05:45:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Mar 2026 05:45:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Mar 2026 05:45:57 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Mar 2026 05:45:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 05:45:57 GMT
WORKDIR /root
# Wed, 11 Mar 2026 05:46:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0891e80814e4c6f8ac7b39a3234a0ed05f01c28ceb68a7414e7253dd49b5574`  
		Last Modified: Wed, 11 Mar 2026 05:51:07 GMT  
		Size: 41.6 MB (41560567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c677769d0438169b5a3d2ea190fd01a6f426789e4d1b44ac567c6fd4199ae7bd`  
		Last Modified: Wed, 11 Mar 2026 05:50:56 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39319aecdf44b1db93065cd12615111cf7735effea6e530a342c3da06cf9897d`  
		Last Modified: Wed, 11 Mar 2026 05:51:28 GMT  
		Size: 180.5 MB (180483788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.2` - unknown; unknown

```console
$ docker pull dart@sha256:36136486b8b169fbe029a4765b424489acb2b4155a666f71dc4e4e82205e1e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd29552cd62ba524024d08385005f46367f6888fe656c0725c3aceefcaa23fe3`

```dockerfile
```

-	Layers:
	-	`sha256:1ac0fb2033730e2430e102f90ba756922f5a29618328ce1fd38dacb64e1a9dcb`  
		Last Modified: Wed, 11 Mar 2026 05:50:55 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.2-sdk`

```console
$ docker pull dart@sha256:318d267b31b9fc3cd86420785fab5c493084b5d3dd16dc6159731ec93f10a2ba
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

### `dart:3.11.2-sdk` - linux; amd64

```console
$ docker pull dart@sha256:0f14c3efce955560a7fdfdca6255ba28fca2dbaa823164385345f8a3aa393053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307068588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd480997ad8dfd9ce83532e18af4fb7f1e571dd92a0d479a7201fdcbbdccc4f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:39:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:39:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:39:59 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:40:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b983e8e71d710fa468d653755314ad0ee7f22241ca986012be178cdce4cb6e`  
		Last Modified: Mon, 16 Mar 2026 22:40:37 GMT  
		Size: 42.5 MB (42491632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e163ed7ccec9c4b4953f644d92db0169ce321a174454a0d9bd26dab1b5e59c3`  
		Last Modified: Mon, 16 Mar 2026 22:40:35 GMT  
		Size: 1.9 MB (1869562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fd2d4c728cf7bbb085d8d05545eb5528550bf00e14b1d65c8593700384d518`  
		Last Modified: Mon, 16 Mar 2026 22:40:40 GMT  
		Size: 232.9 MB (232931862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.2-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e5fed519048230aca05cd25a3511419592f9d2a5d17bd363f7842b45bc567d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332f9ba42d7cf4c4d901003935431ba1fff95df2e17fac09cdaa63e589912bff`

```dockerfile
```

-	Layers:
	-	`sha256:2c50f5fce5f35cb9ef7e2a28701d95ccb2672d1ddd113cf55e8ff2d0db984016`  
		Last Modified: Mon, 16 Mar 2026 22:40:35 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.2-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:4ca8dfc4e10a96b4add5a23e3183aa235c7164e7808063cdeda111f5fd590d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222899348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc2a12b194affa14cdd93476accc96a38c7377a0648d0307a456ae5eac7e36d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:24:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 23:24:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:24:51 GMT
WORKDIR /root
# Mon, 16 Mar 2026 23:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3259b2a1aba5d57e776bc237db3cff79430c80aee94c20a667b063739d161ac9`  
		Last Modified: Mon, 16 Mar 2026 23:25:19 GMT  
		Size: 37.5 MB (37494794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702c1366fd82e973caa542275d0ea83ce3db61fb029842b4a4a65214db82c2d`  
		Last Modified: Mon, 16 Mar 2026 23:25:18 GMT  
		Size: 1.3 MB (1273164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53e6767f19d52512c72d601e689e99b7f93abc3d33625db81c86f146967b4f5`  
		Last Modified: Mon, 16 Mar 2026 23:25:21 GMT  
		Size: 157.9 MB (157921853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.2-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1c0eb28090db31a667732c21e7a5bd7c96d549d60820730d88e25141929c6b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bffbae0171b2ccf3dd57244ed7a66bc3c95b38cd8ae6ab6c8fb355a212e05be`

```dockerfile
```

-	Layers:
	-	`sha256:386cd7fe0a8644f0b603c687a1aa5598bd6e769402ac6db61ac4089cf419be11`  
		Last Modified: Mon, 16 Mar 2026 23:25:18 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.2-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:452d4b44d161dab6cd084bf64c9e57b6a72ed544f9c87b234e3b91583d5c2eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305429760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c7baeb387236b518cb2eebf21cbb60825683085c0c901b8e8a7cbb5e3ed250`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:42:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:42:24 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:42:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:42:24 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:42:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e9cd5e64802379c3eca7f4180704606eef04f0ed0ae6be113d248a71a91433`  
		Last Modified: Mon, 16 Mar 2026 22:43:04 GMT  
		Size: 42.3 MB (42291389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939ba89df0d01d7eb5da514d268117c5dfeb74882a2d15f951e375ee457e3ef1`  
		Last Modified: Mon, 16 Mar 2026 22:43:02 GMT  
		Size: 1.6 MB (1564356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3739a474ab9a11da8519ece2334e297dce18837220bf00b21eb088688f541b38`  
		Last Modified: Mon, 16 Mar 2026 22:43:07 GMT  
		Size: 231.4 MB (231435567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.2-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:f4e8e5e09bdd5f0f84f6567fc2a63f9eb61c8c6ce2c4a34b01c1bfc196bcd8d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34fbe6569738d95356edebe24c3cd07771984fc5f28a7557fff9738352be91c`

```dockerfile
```

-	Layers:
	-	`sha256:b8115bfec7c27f309fb104e42465ad44e5d317aaddf25186f128eda616ef8e2d`  
		Last Modified: Mon, 16 Mar 2026 22:43:02 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.2-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:042f25b2cc5fdf8e71de6bc15fc1c8098e1dfc2831d78647fda0eb971d8e8c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a48f0a5a679b127ba6438717506cc63e6af2971961ded82da8b5e3d06c5f20d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 05:45:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Mar 2026 05:45:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Mar 2026 05:45:57 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Mar 2026 05:45:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 05:45:57 GMT
WORKDIR /root
# Wed, 11 Mar 2026 05:46:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0891e80814e4c6f8ac7b39a3234a0ed05f01c28ceb68a7414e7253dd49b5574`  
		Last Modified: Wed, 11 Mar 2026 05:51:07 GMT  
		Size: 41.6 MB (41560567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c677769d0438169b5a3d2ea190fd01a6f426789e4d1b44ac567c6fd4199ae7bd`  
		Last Modified: Wed, 11 Mar 2026 05:50:56 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39319aecdf44b1db93065cd12615111cf7735effea6e530a342c3da06cf9897d`  
		Last Modified: Wed, 11 Mar 2026 05:51:28 GMT  
		Size: 180.5 MB (180483788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.2-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:36136486b8b169fbe029a4765b424489acb2b4155a666f71dc4e4e82205e1e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd29552cd62ba524024d08385005f46367f6888fe656c0725c3aceefcaa23fe3`

```dockerfile
```

-	Layers:
	-	`sha256:1ac0fb2033730e2430e102f90ba756922f5a29618328ce1fd38dacb64e1a9dcb`  
		Last Modified: Wed, 11 Mar 2026 05:50:55 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.12.0-210.1.beta`

```console
$ docker pull dart@sha256:d75b0bc3861a9b92cd2083e4b8cbe94bb09e6e32a8d44981879a9ea2f827fb9d
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

### `dart:3.12.0-210.1.beta` - linux; amd64

```console
$ docker pull dart@sha256:c12581c602cdbbfcf69da39976f3937363f36d8a01468aa09f70a6e6ca9a2e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311292032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce5d3f9dba77fa44c75ab9f2a366e671dd52351d76d06aab7ce1c81467a493a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:40:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:40:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:40:10 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:40:10 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:40:10 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:40:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbeada001327317f5fc4e02c353e9ec207c90523f9b0836e1bb9407118200f7`  
		Last Modified: Mon, 16 Mar 2026 22:40:54 GMT  
		Size: 42.5 MB (42492272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b52d46f26eae43d5400410e64e26131b27158aa2933687ced81a6105753864c`  
		Last Modified: Mon, 16 Mar 2026 22:40:52 GMT  
		Size: 1.9 MB (1869568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed29a444dfebb0a70c400bbedcef00fda9992baa2eacd86c480970d0167f7d54`  
		Last Modified: Mon, 16 Mar 2026 22:40:58 GMT  
		Size: 237.2 MB (237154660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-210.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:390a7bbad254525f7322a79cd29c4dc9ab532f7ee326924a2c0875ef3bba5b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86af6d9dc5e509df4413377ffd9a175fc2b480f41bfd01954b95052ab4ee1634`

```dockerfile
```

-	Layers:
	-	`sha256:adede3fadc928506661cb5887a08de6a850ebe1730f3d183eaa2c16816e978da`  
		Last Modified: Mon, 16 Mar 2026 22:40:52 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.0-210.1.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:a73159f11ad44cd9cf9f7c28f8aee730f97caaea48bc39aea6b0316b247ee44f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225631076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196818a4c4e9c8903daa528f44a2c37b094244643d7ae6ffafe51981daadf047`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:24:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 23:24:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:24:51 GMT
WORKDIR /root
# Mon, 16 Mar 2026 23:25:36 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3259b2a1aba5d57e776bc237db3cff79430c80aee94c20a667b063739d161ac9`  
		Last Modified: Mon, 16 Mar 2026 23:25:19 GMT  
		Size: 37.5 MB (37494794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702c1366fd82e973caa542275d0ea83ce3db61fb029842b4a4a65214db82c2d`  
		Last Modified: Mon, 16 Mar 2026 23:25:18 GMT  
		Size: 1.3 MB (1273164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa4bddb086ad24d2c2a11b053ada70e6ec23b61885b56a1aaa57fd91ddac6dc`  
		Last Modified: Mon, 16 Mar 2026 23:25:58 GMT  
		Size: 160.7 MB (160653581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-210.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:2b3a17d74e97477a5b0f0010b2ceef247c57263c31978a4e0a4907c6d88536a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd53e9628680bdf82590b5899e5cd5c4120a00c6ffa8d35194b10dd6ac50569`

```dockerfile
```

-	Layers:
	-	`sha256:a79c8670aaa5d09b2310daa6dd70b628139130d2452545c7c221e103c7a5ea91`  
		Last Modified: Mon, 16 Mar 2026 23:25:55 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.0-210.1.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:8e409debb3b1f35d07f04a846ace8a2b2cf11713f9669b9a92ae8ba8d6feed9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 MB (309721393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23ab413a3aee0e81e93cfa7598fade15336d492ad59127d1e0f822f7cd65297`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:42:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:26 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:42:26 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:42:26 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:42:26 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:42:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935879b898a6e8e5f14160da63afde4dda163d7c643a05f45146bebc7ed8a209`  
		Last Modified: Mon, 16 Mar 2026 22:43:12 GMT  
		Size: 42.3 MB (42291472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3146af9ca46109b14bc8124dd1b8855d29f34df395eb9f4ee654a537d5fdddc`  
		Last Modified: Mon, 16 Mar 2026 22:43:10 GMT  
		Size: 1.6 MB (1564345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d807b8e3bd9eb8e5e48bdb9f250cef81aba105e9cd08998352a01caeb0dfbc78`  
		Last Modified: Mon, 16 Mar 2026 22:43:17 GMT  
		Size: 235.7 MB (235727128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-210.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:69659672eb2eb9baf12d2f69f209def53260d095b98c501c63bc3cc15204fdd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2460308aa71bfa9b03a3c24ebe6d675ef6305fae4f1fd0b0b1a07147e387ef8`

```dockerfile
```

-	Layers:
	-	`sha256:31a3aee915bafe141657c00c1602130f7ce11b3da762831034bda12c3adf68c6`  
		Last Modified: Mon, 16 Mar 2026 22:43:10 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.0-210.1.beta` - linux; riscv64

```console
$ docker pull dart@sha256:0d595a10ee452feccc860d03c1786f9f24f6da64636aa890d4df94b217ce801d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256221027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a04e08a82d1320bd6704aa3f3142d2735d65186bddacefe21020046c268ca5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Fri, 06 Mar 2026 00:21:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 00:21:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 06 Mar 2026 00:21:40 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 06 Mar 2026 00:21:40 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 00:21:40 GMT
WORKDIR /root
# Fri, 06 Mar 2026 00:22:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae7c7c60f1ba025c7075344c1c222488ef6b2b6e649d6186b7df38c5479040e`  
		Last Modified: Fri, 06 Mar 2026 00:26:57 GMT  
		Size: 41.6 MB (41560956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f373818ee5733f462d4f19913ff5a8d9bd3456d8b30f568011ff3a08f122a21e`  
		Last Modified: Fri, 06 Mar 2026 00:26:44 GMT  
		Size: 1.6 MB (1564666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b593117537702b6458823200f11bd0f0fb4c6c7a54d7e663cdb082882512f2`  
		Last Modified: Fri, 06 Mar 2026 00:27:18 GMT  
		Size: 184.8 MB (184818956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-210.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:d30b600ae4870cdbd71ebb1dad7b1ef16021e5a8acc058808bd3a4a0961e5482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c86baafc1de1688c5bec8d7b4aafb0eaff60b4da9e2f275cc667673fc40b423`

```dockerfile
```

-	Layers:
	-	`sha256:07f5620c05b4dbb6d90850199e069ba3226f912f7720c5776d0d66eae80c802a`  
		Last Modified: Fri, 06 Mar 2026 00:26:44 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.12.0-210.1.beta-sdk`

```console
$ docker pull dart@sha256:d75b0bc3861a9b92cd2083e4b8cbe94bb09e6e32a8d44981879a9ea2f827fb9d
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

### `dart:3.12.0-210.1.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:c12581c602cdbbfcf69da39976f3937363f36d8a01468aa09f70a6e6ca9a2e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311292032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce5d3f9dba77fa44c75ab9f2a366e671dd52351d76d06aab7ce1c81467a493a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:40:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:40:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:40:10 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:40:10 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:40:10 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:40:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbeada001327317f5fc4e02c353e9ec207c90523f9b0836e1bb9407118200f7`  
		Last Modified: Mon, 16 Mar 2026 22:40:54 GMT  
		Size: 42.5 MB (42492272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b52d46f26eae43d5400410e64e26131b27158aa2933687ced81a6105753864c`  
		Last Modified: Mon, 16 Mar 2026 22:40:52 GMT  
		Size: 1.9 MB (1869568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed29a444dfebb0a70c400bbedcef00fda9992baa2eacd86c480970d0167f7d54`  
		Last Modified: Mon, 16 Mar 2026 22:40:58 GMT  
		Size: 237.2 MB (237154660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-210.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:390a7bbad254525f7322a79cd29c4dc9ab532f7ee326924a2c0875ef3bba5b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86af6d9dc5e509df4413377ffd9a175fc2b480f41bfd01954b95052ab4ee1634`

```dockerfile
```

-	Layers:
	-	`sha256:adede3fadc928506661cb5887a08de6a850ebe1730f3d183eaa2c16816e978da`  
		Last Modified: Mon, 16 Mar 2026 22:40:52 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.0-210.1.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:a73159f11ad44cd9cf9f7c28f8aee730f97caaea48bc39aea6b0316b247ee44f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225631076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196818a4c4e9c8903daa528f44a2c37b094244643d7ae6ffafe51981daadf047`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:24:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 23:24:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:24:51 GMT
WORKDIR /root
# Mon, 16 Mar 2026 23:25:36 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3259b2a1aba5d57e776bc237db3cff79430c80aee94c20a667b063739d161ac9`  
		Last Modified: Mon, 16 Mar 2026 23:25:19 GMT  
		Size: 37.5 MB (37494794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702c1366fd82e973caa542275d0ea83ce3db61fb029842b4a4a65214db82c2d`  
		Last Modified: Mon, 16 Mar 2026 23:25:18 GMT  
		Size: 1.3 MB (1273164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa4bddb086ad24d2c2a11b053ada70e6ec23b61885b56a1aaa57fd91ddac6dc`  
		Last Modified: Mon, 16 Mar 2026 23:25:58 GMT  
		Size: 160.7 MB (160653581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-210.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:2b3a17d74e97477a5b0f0010b2ceef247c57263c31978a4e0a4907c6d88536a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd53e9628680bdf82590b5899e5cd5c4120a00c6ffa8d35194b10dd6ac50569`

```dockerfile
```

-	Layers:
	-	`sha256:a79c8670aaa5d09b2310daa6dd70b628139130d2452545c7c221e103c7a5ea91`  
		Last Modified: Mon, 16 Mar 2026 23:25:55 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.0-210.1.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:8e409debb3b1f35d07f04a846ace8a2b2cf11713f9669b9a92ae8ba8d6feed9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 MB (309721393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23ab413a3aee0e81e93cfa7598fade15336d492ad59127d1e0f822f7cd65297`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:42:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:26 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:42:26 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:42:26 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:42:26 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:42:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935879b898a6e8e5f14160da63afde4dda163d7c643a05f45146bebc7ed8a209`  
		Last Modified: Mon, 16 Mar 2026 22:43:12 GMT  
		Size: 42.3 MB (42291472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3146af9ca46109b14bc8124dd1b8855d29f34df395eb9f4ee654a537d5fdddc`  
		Last Modified: Mon, 16 Mar 2026 22:43:10 GMT  
		Size: 1.6 MB (1564345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d807b8e3bd9eb8e5e48bdb9f250cef81aba105e9cd08998352a01caeb0dfbc78`  
		Last Modified: Mon, 16 Mar 2026 22:43:17 GMT  
		Size: 235.7 MB (235727128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-210.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:69659672eb2eb9baf12d2f69f209def53260d095b98c501c63bc3cc15204fdd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2460308aa71bfa9b03a3c24ebe6d675ef6305fae4f1fd0b0b1a07147e387ef8`

```dockerfile
```

-	Layers:
	-	`sha256:31a3aee915bafe141657c00c1602130f7ce11b3da762831034bda12c3adf68c6`  
		Last Modified: Mon, 16 Mar 2026 22:43:10 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.0-210.1.beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:0d595a10ee452feccc860d03c1786f9f24f6da64636aa890d4df94b217ce801d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256221027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a04e08a82d1320bd6704aa3f3142d2735d65186bddacefe21020046c268ca5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Fri, 06 Mar 2026 00:21:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 00:21:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 06 Mar 2026 00:21:40 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 06 Mar 2026 00:21:40 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 00:21:40 GMT
WORKDIR /root
# Fri, 06 Mar 2026 00:22:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae7c7c60f1ba025c7075344c1c222488ef6b2b6e649d6186b7df38c5479040e`  
		Last Modified: Fri, 06 Mar 2026 00:26:57 GMT  
		Size: 41.6 MB (41560956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f373818ee5733f462d4f19913ff5a8d9bd3456d8b30f568011ff3a08f122a21e`  
		Last Modified: Fri, 06 Mar 2026 00:26:44 GMT  
		Size: 1.6 MB (1564666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b593117537702b6458823200f11bd0f0fb4c6c7a54d7e663cdb082882512f2`  
		Last Modified: Fri, 06 Mar 2026 00:27:18 GMT  
		Size: 184.8 MB (184818956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-210.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:d30b600ae4870cdbd71ebb1dad7b1ef16021e5a8acc058808bd3a4a0961e5482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c86baafc1de1688c5bec8d7b4aafb0eaff60b4da9e2f275cc667673fc40b423`

```dockerfile
```

-	Layers:
	-	`sha256:07f5620c05b4dbb6d90850199e069ba3226f912f7720c5776d0d66eae80c802a`  
		Last Modified: Fri, 06 Mar 2026 00:26:44 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:d75b0bc3861a9b92cd2083e4b8cbe94bb09e6e32a8d44981879a9ea2f827fb9d
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
$ docker pull dart@sha256:c12581c602cdbbfcf69da39976f3937363f36d8a01468aa09f70a6e6ca9a2e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311292032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce5d3f9dba77fa44c75ab9f2a366e671dd52351d76d06aab7ce1c81467a493a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:40:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:40:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:40:10 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:40:10 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:40:10 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:40:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbeada001327317f5fc4e02c353e9ec207c90523f9b0836e1bb9407118200f7`  
		Last Modified: Mon, 16 Mar 2026 22:40:54 GMT  
		Size: 42.5 MB (42492272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b52d46f26eae43d5400410e64e26131b27158aa2933687ced81a6105753864c`  
		Last Modified: Mon, 16 Mar 2026 22:40:52 GMT  
		Size: 1.9 MB (1869568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed29a444dfebb0a70c400bbedcef00fda9992baa2eacd86c480970d0167f7d54`  
		Last Modified: Mon, 16 Mar 2026 22:40:58 GMT  
		Size: 237.2 MB (237154660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:390a7bbad254525f7322a79cd29c4dc9ab532f7ee326924a2c0875ef3bba5b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86af6d9dc5e509df4413377ffd9a175fc2b480f41bfd01954b95052ab4ee1634`

```dockerfile
```

-	Layers:
	-	`sha256:adede3fadc928506661cb5887a08de6a850ebe1730f3d183eaa2c16816e978da`  
		Last Modified: Mon, 16 Mar 2026 22:40:52 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:a73159f11ad44cd9cf9f7c28f8aee730f97caaea48bc39aea6b0316b247ee44f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225631076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196818a4c4e9c8903daa528f44a2c37b094244643d7ae6ffafe51981daadf047`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:24:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 23:24:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:24:51 GMT
WORKDIR /root
# Mon, 16 Mar 2026 23:25:36 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3259b2a1aba5d57e776bc237db3cff79430c80aee94c20a667b063739d161ac9`  
		Last Modified: Mon, 16 Mar 2026 23:25:19 GMT  
		Size: 37.5 MB (37494794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702c1366fd82e973caa542275d0ea83ce3db61fb029842b4a4a65214db82c2d`  
		Last Modified: Mon, 16 Mar 2026 23:25:18 GMT  
		Size: 1.3 MB (1273164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa4bddb086ad24d2c2a11b053ada70e6ec23b61885b56a1aaa57fd91ddac6dc`  
		Last Modified: Mon, 16 Mar 2026 23:25:58 GMT  
		Size: 160.7 MB (160653581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:2b3a17d74e97477a5b0f0010b2ceef247c57263c31978a4e0a4907c6d88536a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd53e9628680bdf82590b5899e5cd5c4120a00c6ffa8d35194b10dd6ac50569`

```dockerfile
```

-	Layers:
	-	`sha256:a79c8670aaa5d09b2310daa6dd70b628139130d2452545c7c221e103c7a5ea91`  
		Last Modified: Mon, 16 Mar 2026 23:25:55 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:8e409debb3b1f35d07f04a846ace8a2b2cf11713f9669b9a92ae8ba8d6feed9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 MB (309721393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23ab413a3aee0e81e93cfa7598fade15336d492ad59127d1e0f822f7cd65297`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:42:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:26 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:42:26 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:42:26 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:42:26 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:42:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935879b898a6e8e5f14160da63afde4dda163d7c643a05f45146bebc7ed8a209`  
		Last Modified: Mon, 16 Mar 2026 22:43:12 GMT  
		Size: 42.3 MB (42291472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3146af9ca46109b14bc8124dd1b8855d29f34df395eb9f4ee654a537d5fdddc`  
		Last Modified: Mon, 16 Mar 2026 22:43:10 GMT  
		Size: 1.6 MB (1564345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d807b8e3bd9eb8e5e48bdb9f250cef81aba105e9cd08998352a01caeb0dfbc78`  
		Last Modified: Mon, 16 Mar 2026 22:43:17 GMT  
		Size: 235.7 MB (235727128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:69659672eb2eb9baf12d2f69f209def53260d095b98c501c63bc3cc15204fdd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2460308aa71bfa9b03a3c24ebe6d675ef6305fae4f1fd0b0b1a07147e387ef8`

```dockerfile
```

-	Layers:
	-	`sha256:31a3aee915bafe141657c00c1602130f7ce11b3da762831034bda12c3adf68c6`  
		Last Modified: Mon, 16 Mar 2026 22:43:10 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:0d595a10ee452feccc860d03c1786f9f24f6da64636aa890d4df94b217ce801d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256221027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a04e08a82d1320bd6704aa3f3142d2735d65186bddacefe21020046c268ca5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Fri, 06 Mar 2026 00:21:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 00:21:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 06 Mar 2026 00:21:40 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 06 Mar 2026 00:21:40 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 00:21:40 GMT
WORKDIR /root
# Fri, 06 Mar 2026 00:22:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae7c7c60f1ba025c7075344c1c222488ef6b2b6e649d6186b7df38c5479040e`  
		Last Modified: Fri, 06 Mar 2026 00:26:57 GMT  
		Size: 41.6 MB (41560956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f373818ee5733f462d4f19913ff5a8d9bd3456d8b30f568011ff3a08f122a21e`  
		Last Modified: Fri, 06 Mar 2026 00:26:44 GMT  
		Size: 1.6 MB (1564666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b593117537702b6458823200f11bd0f0fb4c6c7a54d7e663cdb082882512f2`  
		Last Modified: Fri, 06 Mar 2026 00:27:18 GMT  
		Size: 184.8 MB (184818956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:d30b600ae4870cdbd71ebb1dad7b1ef16021e5a8acc058808bd3a4a0961e5482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c86baafc1de1688c5bec8d7b4aafb0eaff60b4da9e2f275cc667673fc40b423`

```dockerfile
```

-	Layers:
	-	`sha256:07f5620c05b4dbb6d90850199e069ba3226f912f7720c5776d0d66eae80c802a`  
		Last Modified: Fri, 06 Mar 2026 00:26:44 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:d75b0bc3861a9b92cd2083e4b8cbe94bb09e6e32a8d44981879a9ea2f827fb9d
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
$ docker pull dart@sha256:c12581c602cdbbfcf69da39976f3937363f36d8a01468aa09f70a6e6ca9a2e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311292032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce5d3f9dba77fa44c75ab9f2a366e671dd52351d76d06aab7ce1c81467a493a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:40:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:40:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:40:10 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:40:10 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:40:10 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:40:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbeada001327317f5fc4e02c353e9ec207c90523f9b0836e1bb9407118200f7`  
		Last Modified: Mon, 16 Mar 2026 22:40:54 GMT  
		Size: 42.5 MB (42492272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b52d46f26eae43d5400410e64e26131b27158aa2933687ced81a6105753864c`  
		Last Modified: Mon, 16 Mar 2026 22:40:52 GMT  
		Size: 1.9 MB (1869568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed29a444dfebb0a70c400bbedcef00fda9992baa2eacd86c480970d0167f7d54`  
		Last Modified: Mon, 16 Mar 2026 22:40:58 GMT  
		Size: 237.2 MB (237154660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:390a7bbad254525f7322a79cd29c4dc9ab532f7ee326924a2c0875ef3bba5b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86af6d9dc5e509df4413377ffd9a175fc2b480f41bfd01954b95052ab4ee1634`

```dockerfile
```

-	Layers:
	-	`sha256:adede3fadc928506661cb5887a08de6a850ebe1730f3d183eaa2c16816e978da`  
		Last Modified: Mon, 16 Mar 2026 22:40:52 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:a73159f11ad44cd9cf9f7c28f8aee730f97caaea48bc39aea6b0316b247ee44f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225631076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196818a4c4e9c8903daa528f44a2c37b094244643d7ae6ffafe51981daadf047`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:24:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 23:24:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:24:51 GMT
WORKDIR /root
# Mon, 16 Mar 2026 23:25:36 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3259b2a1aba5d57e776bc237db3cff79430c80aee94c20a667b063739d161ac9`  
		Last Modified: Mon, 16 Mar 2026 23:25:19 GMT  
		Size: 37.5 MB (37494794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702c1366fd82e973caa542275d0ea83ce3db61fb029842b4a4a65214db82c2d`  
		Last Modified: Mon, 16 Mar 2026 23:25:18 GMT  
		Size: 1.3 MB (1273164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa4bddb086ad24d2c2a11b053ada70e6ec23b61885b56a1aaa57fd91ddac6dc`  
		Last Modified: Mon, 16 Mar 2026 23:25:58 GMT  
		Size: 160.7 MB (160653581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:2b3a17d74e97477a5b0f0010b2ceef247c57263c31978a4e0a4907c6d88536a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd53e9628680bdf82590b5899e5cd5c4120a00c6ffa8d35194b10dd6ac50569`

```dockerfile
```

-	Layers:
	-	`sha256:a79c8670aaa5d09b2310daa6dd70b628139130d2452545c7c221e103c7a5ea91`  
		Last Modified: Mon, 16 Mar 2026 23:25:55 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:8e409debb3b1f35d07f04a846ace8a2b2cf11713f9669b9a92ae8ba8d6feed9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 MB (309721393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23ab413a3aee0e81e93cfa7598fade15336d492ad59127d1e0f822f7cd65297`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:42:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:26 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:42:26 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:42:26 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:42:26 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:42:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935879b898a6e8e5f14160da63afde4dda163d7c643a05f45146bebc7ed8a209`  
		Last Modified: Mon, 16 Mar 2026 22:43:12 GMT  
		Size: 42.3 MB (42291472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3146af9ca46109b14bc8124dd1b8855d29f34df395eb9f4ee654a537d5fdddc`  
		Last Modified: Mon, 16 Mar 2026 22:43:10 GMT  
		Size: 1.6 MB (1564345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d807b8e3bd9eb8e5e48bdb9f250cef81aba105e9cd08998352a01caeb0dfbc78`  
		Last Modified: Mon, 16 Mar 2026 22:43:17 GMT  
		Size: 235.7 MB (235727128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:69659672eb2eb9baf12d2f69f209def53260d095b98c501c63bc3cc15204fdd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2460308aa71bfa9b03a3c24ebe6d675ef6305fae4f1fd0b0b1a07147e387ef8`

```dockerfile
```

-	Layers:
	-	`sha256:31a3aee915bafe141657c00c1602130f7ce11b3da762831034bda12c3adf68c6`  
		Last Modified: Mon, 16 Mar 2026 22:43:10 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:0d595a10ee452feccc860d03c1786f9f24f6da64636aa890d4df94b217ce801d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256221027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a04e08a82d1320bd6704aa3f3142d2735d65186bddacefe21020046c268ca5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Fri, 06 Mar 2026 00:21:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 00:21:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 06 Mar 2026 00:21:40 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 06 Mar 2026 00:21:40 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 00:21:40 GMT
WORKDIR /root
# Fri, 06 Mar 2026 00:22:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae7c7c60f1ba025c7075344c1c222488ef6b2b6e649d6186b7df38c5479040e`  
		Last Modified: Fri, 06 Mar 2026 00:26:57 GMT  
		Size: 41.6 MB (41560956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f373818ee5733f462d4f19913ff5a8d9bd3456d8b30f568011ff3a08f122a21e`  
		Last Modified: Fri, 06 Mar 2026 00:26:44 GMT  
		Size: 1.6 MB (1564666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b593117537702b6458823200f11bd0f0fb4c6c7a54d7e663cdb082882512f2`  
		Last Modified: Fri, 06 Mar 2026 00:27:18 GMT  
		Size: 184.8 MB (184818956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:d30b600ae4870cdbd71ebb1dad7b1ef16021e5a8acc058808bd3a4a0961e5482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c86baafc1de1688c5bec8d7b4aafb0eaff60b4da9e2f275cc667673fc40b423`

```dockerfile
```

-	Layers:
	-	`sha256:07f5620c05b4dbb6d90850199e069ba3226f912f7720c5776d0d66eae80c802a`  
		Last Modified: Fri, 06 Mar 2026 00:26:44 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:318d267b31b9fc3cd86420785fab5c493084b5d3dd16dc6159731ec93f10a2ba
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
$ docker pull dart@sha256:0f14c3efce955560a7fdfdca6255ba28fca2dbaa823164385345f8a3aa393053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307068588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd480997ad8dfd9ce83532e18af4fb7f1e571dd92a0d479a7201fdcbbdccc4f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:39:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:39:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:39:59 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:40:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b983e8e71d710fa468d653755314ad0ee7f22241ca986012be178cdce4cb6e`  
		Last Modified: Mon, 16 Mar 2026 22:40:37 GMT  
		Size: 42.5 MB (42491632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e163ed7ccec9c4b4953f644d92db0169ce321a174454a0d9bd26dab1b5e59c3`  
		Last Modified: Mon, 16 Mar 2026 22:40:35 GMT  
		Size: 1.9 MB (1869562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fd2d4c728cf7bbb085d8d05545eb5528550bf00e14b1d65c8593700384d518`  
		Last Modified: Mon, 16 Mar 2026 22:40:40 GMT  
		Size: 232.9 MB (232931862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:e5fed519048230aca05cd25a3511419592f9d2a5d17bd363f7842b45bc567d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332f9ba42d7cf4c4d901003935431ba1fff95df2e17fac09cdaa63e589912bff`

```dockerfile
```

-	Layers:
	-	`sha256:2c50f5fce5f35cb9ef7e2a28701d95ccb2672d1ddd113cf55e8ff2d0db984016`  
		Last Modified: Mon, 16 Mar 2026 22:40:35 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:4ca8dfc4e10a96b4add5a23e3183aa235c7164e7808063cdeda111f5fd590d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222899348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc2a12b194affa14cdd93476accc96a38c7377a0648d0307a456ae5eac7e36d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:24:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 23:24:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:24:51 GMT
WORKDIR /root
# Mon, 16 Mar 2026 23:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3259b2a1aba5d57e776bc237db3cff79430c80aee94c20a667b063739d161ac9`  
		Last Modified: Mon, 16 Mar 2026 23:25:19 GMT  
		Size: 37.5 MB (37494794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702c1366fd82e973caa542275d0ea83ce3db61fb029842b4a4a65214db82c2d`  
		Last Modified: Mon, 16 Mar 2026 23:25:18 GMT  
		Size: 1.3 MB (1273164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53e6767f19d52512c72d601e689e99b7f93abc3d33625db81c86f146967b4f5`  
		Last Modified: Mon, 16 Mar 2026 23:25:21 GMT  
		Size: 157.9 MB (157921853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:1c0eb28090db31a667732c21e7a5bd7c96d549d60820730d88e25141929c6b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bffbae0171b2ccf3dd57244ed7a66bc3c95b38cd8ae6ab6c8fb355a212e05be`

```dockerfile
```

-	Layers:
	-	`sha256:386cd7fe0a8644f0b603c687a1aa5598bd6e769402ac6db61ac4089cf419be11`  
		Last Modified: Mon, 16 Mar 2026 23:25:18 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:452d4b44d161dab6cd084bf64c9e57b6a72ed544f9c87b234e3b91583d5c2eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305429760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c7baeb387236b518cb2eebf21cbb60825683085c0c901b8e8a7cbb5e3ed250`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:42:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:42:24 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:42:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:42:24 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:42:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e9cd5e64802379c3eca7f4180704606eef04f0ed0ae6be113d248a71a91433`  
		Last Modified: Mon, 16 Mar 2026 22:43:04 GMT  
		Size: 42.3 MB (42291389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939ba89df0d01d7eb5da514d268117c5dfeb74882a2d15f951e375ee457e3ef1`  
		Last Modified: Mon, 16 Mar 2026 22:43:02 GMT  
		Size: 1.6 MB (1564356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3739a474ab9a11da8519ece2334e297dce18837220bf00b21eb088688f541b38`  
		Last Modified: Mon, 16 Mar 2026 22:43:07 GMT  
		Size: 231.4 MB (231435567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:f4e8e5e09bdd5f0f84f6567fc2a63f9eb61c8c6ce2c4a34b01c1bfc196bcd8d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34fbe6569738d95356edebe24c3cd07771984fc5f28a7557fff9738352be91c`

```dockerfile
```

-	Layers:
	-	`sha256:b8115bfec7c27f309fb104e42465ad44e5d317aaddf25186f128eda616ef8e2d`  
		Last Modified: Mon, 16 Mar 2026 22:43:02 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; riscv64

```console
$ docker pull dart@sha256:042f25b2cc5fdf8e71de6bc15fc1c8098e1dfc2831d78647fda0eb971d8e8c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a48f0a5a679b127ba6438717506cc63e6af2971961ded82da8b5e3d06c5f20d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 05:45:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Mar 2026 05:45:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Mar 2026 05:45:57 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Mar 2026 05:45:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 05:45:57 GMT
WORKDIR /root
# Wed, 11 Mar 2026 05:46:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0891e80814e4c6f8ac7b39a3234a0ed05f01c28ceb68a7414e7253dd49b5574`  
		Last Modified: Wed, 11 Mar 2026 05:51:07 GMT  
		Size: 41.6 MB (41560567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c677769d0438169b5a3d2ea190fd01a6f426789e4d1b44ac567c6fd4199ae7bd`  
		Last Modified: Wed, 11 Mar 2026 05:50:56 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39319aecdf44b1db93065cd12615111cf7735effea6e530a342c3da06cf9897d`  
		Last Modified: Wed, 11 Mar 2026 05:51:28 GMT  
		Size: 180.5 MB (180483788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:36136486b8b169fbe029a4765b424489acb2b4155a666f71dc4e4e82205e1e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd29552cd62ba524024d08385005f46367f6888fe656c0725c3aceefcaa23fe3`

```dockerfile
```

-	Layers:
	-	`sha256:1ac0fb2033730e2430e102f90ba756922f5a29618328ce1fd38dacb64e1a9dcb`  
		Last Modified: Wed, 11 Mar 2026 05:50:55 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:318d267b31b9fc3cd86420785fab5c493084b5d3dd16dc6159731ec93f10a2ba
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
$ docker pull dart@sha256:0f14c3efce955560a7fdfdca6255ba28fca2dbaa823164385345f8a3aa393053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307068588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd480997ad8dfd9ce83532e18af4fb7f1e571dd92a0d479a7201fdcbbdccc4f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:39:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:39:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:39:59 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:40:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b983e8e71d710fa468d653755314ad0ee7f22241ca986012be178cdce4cb6e`  
		Last Modified: Mon, 16 Mar 2026 22:40:37 GMT  
		Size: 42.5 MB (42491632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e163ed7ccec9c4b4953f644d92db0169ce321a174454a0d9bd26dab1b5e59c3`  
		Last Modified: Mon, 16 Mar 2026 22:40:35 GMT  
		Size: 1.9 MB (1869562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fd2d4c728cf7bbb085d8d05545eb5528550bf00e14b1d65c8593700384d518`  
		Last Modified: Mon, 16 Mar 2026 22:40:40 GMT  
		Size: 232.9 MB (232931862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e5fed519048230aca05cd25a3511419592f9d2a5d17bd363f7842b45bc567d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332f9ba42d7cf4c4d901003935431ba1fff95df2e17fac09cdaa63e589912bff`

```dockerfile
```

-	Layers:
	-	`sha256:2c50f5fce5f35cb9ef7e2a28701d95ccb2672d1ddd113cf55e8ff2d0db984016`  
		Last Modified: Mon, 16 Mar 2026 22:40:35 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:4ca8dfc4e10a96b4add5a23e3183aa235c7164e7808063cdeda111f5fd590d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222899348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc2a12b194affa14cdd93476accc96a38c7377a0648d0307a456ae5eac7e36d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:24:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 23:24:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:24:51 GMT
WORKDIR /root
# Mon, 16 Mar 2026 23:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3259b2a1aba5d57e776bc237db3cff79430c80aee94c20a667b063739d161ac9`  
		Last Modified: Mon, 16 Mar 2026 23:25:19 GMT  
		Size: 37.5 MB (37494794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702c1366fd82e973caa542275d0ea83ce3db61fb029842b4a4a65214db82c2d`  
		Last Modified: Mon, 16 Mar 2026 23:25:18 GMT  
		Size: 1.3 MB (1273164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53e6767f19d52512c72d601e689e99b7f93abc3d33625db81c86f146967b4f5`  
		Last Modified: Mon, 16 Mar 2026 23:25:21 GMT  
		Size: 157.9 MB (157921853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1c0eb28090db31a667732c21e7a5bd7c96d549d60820730d88e25141929c6b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bffbae0171b2ccf3dd57244ed7a66bc3c95b38cd8ae6ab6c8fb355a212e05be`

```dockerfile
```

-	Layers:
	-	`sha256:386cd7fe0a8644f0b603c687a1aa5598bd6e769402ac6db61ac4089cf419be11`  
		Last Modified: Mon, 16 Mar 2026 23:25:18 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:452d4b44d161dab6cd084bf64c9e57b6a72ed544f9c87b234e3b91583d5c2eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305429760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c7baeb387236b518cb2eebf21cbb60825683085c0c901b8e8a7cbb5e3ed250`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:42:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:42:24 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:42:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:42:24 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:42:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e9cd5e64802379c3eca7f4180704606eef04f0ed0ae6be113d248a71a91433`  
		Last Modified: Mon, 16 Mar 2026 22:43:04 GMT  
		Size: 42.3 MB (42291389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939ba89df0d01d7eb5da514d268117c5dfeb74882a2d15f951e375ee457e3ef1`  
		Last Modified: Mon, 16 Mar 2026 22:43:02 GMT  
		Size: 1.6 MB (1564356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3739a474ab9a11da8519ece2334e297dce18837220bf00b21eb088688f541b38`  
		Last Modified: Mon, 16 Mar 2026 22:43:07 GMT  
		Size: 231.4 MB (231435567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:f4e8e5e09bdd5f0f84f6567fc2a63f9eb61c8c6ce2c4a34b01c1bfc196bcd8d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34fbe6569738d95356edebe24c3cd07771984fc5f28a7557fff9738352be91c`

```dockerfile
```

-	Layers:
	-	`sha256:b8115bfec7c27f309fb104e42465ad44e5d317aaddf25186f128eda616ef8e2d`  
		Last Modified: Mon, 16 Mar 2026 22:43:02 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; riscv64

```console
$ docker pull dart@sha256:042f25b2cc5fdf8e71de6bc15fc1c8098e1dfc2831d78647fda0eb971d8e8c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a48f0a5a679b127ba6438717506cc63e6af2971961ded82da8b5e3d06c5f20d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 05:45:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Mar 2026 05:45:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Mar 2026 05:45:57 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Mar 2026 05:45:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 05:45:57 GMT
WORKDIR /root
# Wed, 11 Mar 2026 05:46:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0891e80814e4c6f8ac7b39a3234a0ed05f01c28ceb68a7414e7253dd49b5574`  
		Last Modified: Wed, 11 Mar 2026 05:51:07 GMT  
		Size: 41.6 MB (41560567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c677769d0438169b5a3d2ea190fd01a6f426789e4d1b44ac567c6fd4199ae7bd`  
		Last Modified: Wed, 11 Mar 2026 05:50:56 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39319aecdf44b1db93065cd12615111cf7735effea6e530a342c3da06cf9897d`  
		Last Modified: Wed, 11 Mar 2026 05:51:28 GMT  
		Size: 180.5 MB (180483788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:36136486b8b169fbe029a4765b424489acb2b4155a666f71dc4e4e82205e1e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd29552cd62ba524024d08385005f46367f6888fe656c0725c3aceefcaa23fe3`

```dockerfile
```

-	Layers:
	-	`sha256:1ac0fb2033730e2430e102f90ba756922f5a29618328ce1fd38dacb64e1a9dcb`  
		Last Modified: Wed, 11 Mar 2026 05:50:55 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:318d267b31b9fc3cd86420785fab5c493084b5d3dd16dc6159731ec93f10a2ba
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
$ docker pull dart@sha256:0f14c3efce955560a7fdfdca6255ba28fca2dbaa823164385345f8a3aa393053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307068588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd480997ad8dfd9ce83532e18af4fb7f1e571dd92a0d479a7201fdcbbdccc4f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:39:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:39:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:39:59 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:40:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b983e8e71d710fa468d653755314ad0ee7f22241ca986012be178cdce4cb6e`  
		Last Modified: Mon, 16 Mar 2026 22:40:37 GMT  
		Size: 42.5 MB (42491632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e163ed7ccec9c4b4953f644d92db0169ce321a174454a0d9bd26dab1b5e59c3`  
		Last Modified: Mon, 16 Mar 2026 22:40:35 GMT  
		Size: 1.9 MB (1869562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fd2d4c728cf7bbb085d8d05545eb5528550bf00e14b1d65c8593700384d518`  
		Last Modified: Mon, 16 Mar 2026 22:40:40 GMT  
		Size: 232.9 MB (232931862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:e5fed519048230aca05cd25a3511419592f9d2a5d17bd363f7842b45bc567d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332f9ba42d7cf4c4d901003935431ba1fff95df2e17fac09cdaa63e589912bff`

```dockerfile
```

-	Layers:
	-	`sha256:2c50f5fce5f35cb9ef7e2a28701d95ccb2672d1ddd113cf55e8ff2d0db984016`  
		Last Modified: Mon, 16 Mar 2026 22:40:35 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:4ca8dfc4e10a96b4add5a23e3183aa235c7164e7808063cdeda111f5fd590d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222899348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc2a12b194affa14cdd93476accc96a38c7377a0648d0307a456ae5eac7e36d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:24:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 23:24:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:24:51 GMT
WORKDIR /root
# Mon, 16 Mar 2026 23:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3259b2a1aba5d57e776bc237db3cff79430c80aee94c20a667b063739d161ac9`  
		Last Modified: Mon, 16 Mar 2026 23:25:19 GMT  
		Size: 37.5 MB (37494794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702c1366fd82e973caa542275d0ea83ce3db61fb029842b4a4a65214db82c2d`  
		Last Modified: Mon, 16 Mar 2026 23:25:18 GMT  
		Size: 1.3 MB (1273164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53e6767f19d52512c72d601e689e99b7f93abc3d33625db81c86f146967b4f5`  
		Last Modified: Mon, 16 Mar 2026 23:25:21 GMT  
		Size: 157.9 MB (157921853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:1c0eb28090db31a667732c21e7a5bd7c96d549d60820730d88e25141929c6b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bffbae0171b2ccf3dd57244ed7a66bc3c95b38cd8ae6ab6c8fb355a212e05be`

```dockerfile
```

-	Layers:
	-	`sha256:386cd7fe0a8644f0b603c687a1aa5598bd6e769402ac6db61ac4089cf419be11`  
		Last Modified: Mon, 16 Mar 2026 23:25:18 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:452d4b44d161dab6cd084bf64c9e57b6a72ed544f9c87b234e3b91583d5c2eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305429760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c7baeb387236b518cb2eebf21cbb60825683085c0c901b8e8a7cbb5e3ed250`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:42:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:42:24 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:42:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:42:24 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:42:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e9cd5e64802379c3eca7f4180704606eef04f0ed0ae6be113d248a71a91433`  
		Last Modified: Mon, 16 Mar 2026 22:43:04 GMT  
		Size: 42.3 MB (42291389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939ba89df0d01d7eb5da514d268117c5dfeb74882a2d15f951e375ee457e3ef1`  
		Last Modified: Mon, 16 Mar 2026 22:43:02 GMT  
		Size: 1.6 MB (1564356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3739a474ab9a11da8519ece2334e297dce18837220bf00b21eb088688f541b38`  
		Last Modified: Mon, 16 Mar 2026 22:43:07 GMT  
		Size: 231.4 MB (231435567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:f4e8e5e09bdd5f0f84f6567fc2a63f9eb61c8c6ce2c4a34b01c1bfc196bcd8d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34fbe6569738d95356edebe24c3cd07771984fc5f28a7557fff9738352be91c`

```dockerfile
```

-	Layers:
	-	`sha256:b8115bfec7c27f309fb104e42465ad44e5d317aaddf25186f128eda616ef8e2d`  
		Last Modified: Mon, 16 Mar 2026 22:43:02 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; riscv64

```console
$ docker pull dart@sha256:042f25b2cc5fdf8e71de6bc15fc1c8098e1dfc2831d78647fda0eb971d8e8c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a48f0a5a679b127ba6438717506cc63e6af2971961ded82da8b5e3d06c5f20d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 05:45:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Mar 2026 05:45:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Mar 2026 05:45:57 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Mar 2026 05:45:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 05:45:57 GMT
WORKDIR /root
# Wed, 11 Mar 2026 05:46:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0891e80814e4c6f8ac7b39a3234a0ed05f01c28ceb68a7414e7253dd49b5574`  
		Last Modified: Wed, 11 Mar 2026 05:51:07 GMT  
		Size: 41.6 MB (41560567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c677769d0438169b5a3d2ea190fd01a6f426789e4d1b44ac567c6fd4199ae7bd`  
		Last Modified: Wed, 11 Mar 2026 05:50:56 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39319aecdf44b1db93065cd12615111cf7735effea6e530a342c3da06cf9897d`  
		Last Modified: Wed, 11 Mar 2026 05:51:28 GMT  
		Size: 180.5 MB (180483788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:36136486b8b169fbe029a4765b424489acb2b4155a666f71dc4e4e82205e1e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd29552cd62ba524024d08385005f46367f6888fe656c0725c3aceefcaa23fe3`

```dockerfile
```

-	Layers:
	-	`sha256:1ac0fb2033730e2430e102f90ba756922f5a29618328ce1fd38dacb64e1a9dcb`  
		Last Modified: Wed, 11 Mar 2026 05:50:55 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:318d267b31b9fc3cd86420785fab5c493084b5d3dd16dc6159731ec93f10a2ba
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
$ docker pull dart@sha256:0f14c3efce955560a7fdfdca6255ba28fca2dbaa823164385345f8a3aa393053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307068588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd480997ad8dfd9ce83532e18af4fb7f1e571dd92a0d479a7201fdcbbdccc4f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:39:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:39:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:39:59 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:40:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b983e8e71d710fa468d653755314ad0ee7f22241ca986012be178cdce4cb6e`  
		Last Modified: Mon, 16 Mar 2026 22:40:37 GMT  
		Size: 42.5 MB (42491632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e163ed7ccec9c4b4953f644d92db0169ce321a174454a0d9bd26dab1b5e59c3`  
		Last Modified: Mon, 16 Mar 2026 22:40:35 GMT  
		Size: 1.9 MB (1869562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fd2d4c728cf7bbb085d8d05545eb5528550bf00e14b1d65c8593700384d518`  
		Last Modified: Mon, 16 Mar 2026 22:40:40 GMT  
		Size: 232.9 MB (232931862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e5fed519048230aca05cd25a3511419592f9d2a5d17bd363f7842b45bc567d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332f9ba42d7cf4c4d901003935431ba1fff95df2e17fac09cdaa63e589912bff`

```dockerfile
```

-	Layers:
	-	`sha256:2c50f5fce5f35cb9ef7e2a28701d95ccb2672d1ddd113cf55e8ff2d0db984016`  
		Last Modified: Mon, 16 Mar 2026 22:40:35 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:4ca8dfc4e10a96b4add5a23e3183aa235c7164e7808063cdeda111f5fd590d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222899348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc2a12b194affa14cdd93476accc96a38c7377a0648d0307a456ae5eac7e36d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:24:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 23:24:51 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 23:24:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:24:51 GMT
WORKDIR /root
# Mon, 16 Mar 2026 23:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3259b2a1aba5d57e776bc237db3cff79430c80aee94c20a667b063739d161ac9`  
		Last Modified: Mon, 16 Mar 2026 23:25:19 GMT  
		Size: 37.5 MB (37494794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702c1366fd82e973caa542275d0ea83ce3db61fb029842b4a4a65214db82c2d`  
		Last Modified: Mon, 16 Mar 2026 23:25:18 GMT  
		Size: 1.3 MB (1273164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53e6767f19d52512c72d601e689e99b7f93abc3d33625db81c86f146967b4f5`  
		Last Modified: Mon, 16 Mar 2026 23:25:21 GMT  
		Size: 157.9 MB (157921853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1c0eb28090db31a667732c21e7a5bd7c96d549d60820730d88e25141929c6b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bffbae0171b2ccf3dd57244ed7a66bc3c95b38cd8ae6ab6c8fb355a212e05be`

```dockerfile
```

-	Layers:
	-	`sha256:386cd7fe0a8644f0b603c687a1aa5598bd6e769402ac6db61ac4089cf419be11`  
		Last Modified: Mon, 16 Mar 2026 23:25:18 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:452d4b44d161dab6cd084bf64c9e57b6a72ed544f9c87b234e3b91583d5c2eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305429760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c7baeb387236b518cb2eebf21cbb60825683085c0c901b8e8a7cbb5e3ed250`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:42:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 16 Mar 2026 22:42:24 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 16 Mar 2026 22:42:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:42:24 GMT
WORKDIR /root
# Mon, 16 Mar 2026 22:42:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e9cd5e64802379c3eca7f4180704606eef04f0ed0ae6be113d248a71a91433`  
		Last Modified: Mon, 16 Mar 2026 22:43:04 GMT  
		Size: 42.3 MB (42291389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939ba89df0d01d7eb5da514d268117c5dfeb74882a2d15f951e375ee457e3ef1`  
		Last Modified: Mon, 16 Mar 2026 22:43:02 GMT  
		Size: 1.6 MB (1564356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3739a474ab9a11da8519ece2334e297dce18837220bf00b21eb088688f541b38`  
		Last Modified: Mon, 16 Mar 2026 22:43:07 GMT  
		Size: 231.4 MB (231435567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:f4e8e5e09bdd5f0f84f6567fc2a63f9eb61c8c6ce2c4a34b01c1bfc196bcd8d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34fbe6569738d95356edebe24c3cd07771984fc5f28a7557fff9738352be91c`

```dockerfile
```

-	Layers:
	-	`sha256:b8115bfec7c27f309fb104e42465ad44e5d317aaddf25186f128eda616ef8e2d`  
		Last Modified: Mon, 16 Mar 2026 22:43:02 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:042f25b2cc5fdf8e71de6bc15fc1c8098e1dfc2831d78647fda0eb971d8e8c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a48f0a5a679b127ba6438717506cc63e6af2971961ded82da8b5e3d06c5f20d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 05:45:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Mar 2026 05:45:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Mar 2026 05:45:57 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Mar 2026 05:45:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 05:45:57 GMT
WORKDIR /root
# Wed, 11 Mar 2026 05:46:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0891e80814e4c6f8ac7b39a3234a0ed05f01c28ceb68a7414e7253dd49b5574`  
		Last Modified: Wed, 11 Mar 2026 05:51:07 GMT  
		Size: 41.6 MB (41560567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c677769d0438169b5a3d2ea190fd01a6f426789e4d1b44ac567c6fd4199ae7bd`  
		Last Modified: Wed, 11 Mar 2026 05:50:56 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39319aecdf44b1db93065cd12615111cf7735effea6e530a342c3da06cf9897d`  
		Last Modified: Wed, 11 Mar 2026 05:51:28 GMT  
		Size: 180.5 MB (180483788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:36136486b8b169fbe029a4765b424489acb2b4155a666f71dc4e4e82205e1e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd29552cd62ba524024d08385005f46367f6888fe656c0725c3aceefcaa23fe3`

```dockerfile
```

-	Layers:
	-	`sha256:1ac0fb2033730e2430e102f90ba756922f5a29618328ce1fd38dacb64e1a9dcb`  
		Last Modified: Wed, 11 Mar 2026 05:50:55 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json
