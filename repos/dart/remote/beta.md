## `dart:beta`

```console
$ docker pull dart@sha256:3476d4fc2e56cee47d88594ad967847585d39da3e98f86c6f285085c78a0ea40
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
$ docker pull dart@sha256:da8b1a22344a2f13593e089c2f817e605143a97cba2df6747180ac1e2164b289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307090359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711f1ef91674dc25d2ed793614a27df6308e3346d316c5ef5e621f83e1651281`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 17:50:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 17:50:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 17:50:28 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 17:50:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 17:50:28 GMT
WORKDIR /root
# Tue, 13 Jan 2026 17:50:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1d7139fda640af2f0039bbb842901f61a88ef59a20525ca35c6a6047163e76;             SDK_ARCH="x64";;         armhf)             DART_SHA256=be890d3df1f4397a25a3e3104e252e2421166a1b1e88143dc4dac72ae1682c50;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c06fe3aee69a0bb0ded664a28eba38176558ccbe69a8eb6f0d26c700956a5fe8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=09e74f6b142c79b524242a03abb1fe409ccd0fb8fc5661343fa8b680e511ec62;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31717fe3f63bc4b46ba25be85b210cb57797f444c36a4dfca836b72ac733b03`  
		Last Modified: Tue, 13 Jan 2026 17:51:29 GMT  
		Size: 42.5 MB (42496178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712442cdf2e67321fc56d12eea5e67631773644bb9f28b6842144404aa3f3e93`  
		Last Modified: Tue, 13 Jan 2026 17:51:23 GMT  
		Size: 1.9 MB (1870175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91853fa2cdb23195015c727705b9cce17ae6829dbba5a6bbb3660b1df49c934`  
		Last Modified: Tue, 13 Jan 2026 17:58:23 GMT  
		Size: 233.0 MB (232950289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:d48e28dd4c8aeebeb01e37093c655c63e1c6c200deff05f22703d090da0f616b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b7073e3ee1c8b6e0ebdd4769999ebcfaf4fbdddb7ac9be324422810b463aa2`

```dockerfile
```

-	Layers:
	-	`sha256:bad1d6b497339b3fc55f95cc21a9d8ad6d9b07b7f00a52eb20dcba2947bc2602`  
		Last Modified: Tue, 13 Jan 2026 21:53:26 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:acc516f1026f5e3eadd227704c78e6bebd52b6d0346d82dc5263cae0670b7d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222899574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23901c4ad5601b3e2aada638af5790902c5c30ab93264e6be989b09ddb5b908`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 17:57:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 17:57:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 17:57:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 17:57:11 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 17:57:11 GMT
WORKDIR /root
# Tue, 13 Jan 2026 17:57:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1d7139fda640af2f0039bbb842901f61a88ef59a20525ca35c6a6047163e76;             SDK_ARCH="x64";;         armhf)             DART_SHA256=be890d3df1f4397a25a3e3104e252e2421166a1b1e88143dc4dac72ae1682c50;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c06fe3aee69a0bb0ded664a28eba38176558ccbe69a8eb6f0d26c700956a5fe8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=09e74f6b142c79b524242a03abb1fe409ccd0fb8fc5661343fa8b680e511ec62;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61e99571e238da169385ef419321eb10f3cfa2347dabc10701a7d179c3d5c05`  
		Last Modified: Tue, 13 Jan 2026 17:58:00 GMT  
		Size: 37.5 MB (37497570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67315b84b37e5589e484d4ae8df9649947bec4b75a138f4cc185708eb8f8b9b5`  
		Last Modified: Tue, 13 Jan 2026 17:57:58 GMT  
		Size: 1.3 MB (1273160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137940b2a3a956f47e6e7ece44e42fa1447e20c516d533f23fa8eee1883276e2`  
		Last Modified: Tue, 13 Jan 2026 18:03:14 GMT  
		Size: 157.9 MB (157920234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:94fb5b34db15dd619559217fe18a56898177ffea36a29d9f81f77ab6fff1d038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac4295162cb419fb0455b29e9f9852e204a82482da33629844b4af4112de7cf`

```dockerfile
```

-	Layers:
	-	`sha256:804b0478f56366200665c1a79b9b6861f500a1aa16bcd958ebd200680d8a7a78`  
		Last Modified: Tue, 13 Jan 2026 21:53:30 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:de918bbd30afe37e8870c7eadc5d976241f64676d7f98ebcac7934d3e288eafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305439814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a64ad138cc690fc78f75a9cef4b33af319ce4bffeb311a74371096d3add5664`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 17:50:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 17:50:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 17:50:53 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 17:50:53 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 17:50:53 GMT
WORKDIR /root
# Tue, 13 Jan 2026 17:51:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1d7139fda640af2f0039bbb842901f61a88ef59a20525ca35c6a6047163e76;             SDK_ARCH="x64";;         armhf)             DART_SHA256=be890d3df1f4397a25a3e3104e252e2421166a1b1e88143dc4dac72ae1682c50;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c06fe3aee69a0bb0ded664a28eba38176558ccbe69a8eb6f0d26c700956a5fe8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=09e74f6b142c79b524242a03abb1fe409ccd0fb8fc5661343fa8b680e511ec62;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79982bc37f5efef6e806934713fe6a28e5ac139088dfaf71d2b351a0911c6393`  
		Last Modified: Tue, 13 Jan 2026 17:51:53 GMT  
		Size: 42.3 MB (42292862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e501186dc201888f65f869cd4e59980bfc8a046ff6933b917fab2703635be43d`  
		Last Modified: Tue, 13 Jan 2026 17:51:48 GMT  
		Size: 1.6 MB (1564520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59910d566c09cf83ab2de3c61a6165260bc3ec2eb2fbad0f3dcae98f85b7a0d`  
		Last Modified: Tue, 13 Jan 2026 17:57:32 GMT  
		Size: 231.4 MB (231448358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:69f73cfd0a536eba875eb069b5d87f59a04d28a65a78223e0d09eef06de0f096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8130eb1305a3635d1bbd42f45d6dc76e9f3cd8ddaea8efd667d1dbfbe46a54`

```dockerfile
```

-	Layers:
	-	`sha256:5a34a501e29491bfd0c311495aa36a82f474582701e69ec3462f9a7da2430799`  
		Last Modified: Tue, 13 Jan 2026 21:53:39 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:2cfdd54bdc709dd57f5e9967e59dcf202795d53070353a674b7466068ed75939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251894743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b877615a26388ddead16a06e335acd030c2aaa08ad3ed4964cf6845f15b057d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 07 Jan 2026 17:53:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Jan 2026 17:53:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 07 Jan 2026 17:53:21 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 07 Jan 2026 17:53:21 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jan 2026 17:53:21 GMT
WORKDIR /root
# Thu, 08 Jan 2026 19:03:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=edd704e758363f4e91f7e331e8c0c1dd6f65459a2c45a12ca8800c98ea6aa994;             SDK_ARCH="x64";;         armhf)             DART_SHA256=668f984cb8252e3b1ad067a1fee4985a58453ac8575042d4c12781297f8b7f65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=30b6e1e200a55108989e52094186fbb3f71819c1d75ba1fe9f084f8b77930415;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=ac3fd240cb4ad31e7b64d33f11a266e007f80a4554d6e53c2accf57f57a2d396;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7371402766e4abc95eaf0d0fca5d28b341ec201064383d231f20c9f6c9cbfd42`  
		Last Modified: Wed, 07 Jan 2026 17:59:02 GMT  
		Size: 41.6 MB (41560755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33684bab959ef2a5be84df6d39f37456a938f2f54f81fa698516adc65104c8b`  
		Last Modified: Wed, 07 Jan 2026 17:58:56 GMT  
		Size: 1.6 MB (1567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20287815c4db5622d2036c3b61c21b86ac227bcbfc7a019cc23c3d372c0027`  
		Last Modified: Thu, 08 Jan 2026 19:09:04 GMT  
		Size: 180.5 MB (180493757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:9ffb45d7609846f4cdfeec23d2d0f8a0f20aa8ff3b1abc4e57712587b0a74a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac32ba00dccfda38803d938d9c652855a1927a5b4ed811dc448294c7c79d096`

```dockerfile
```

-	Layers:
	-	`sha256:05c7bb5d7458d535a1e4271e1e71355be0072e8f31152f6a4ecca5a2c3a14823`  
		Last Modified: Thu, 08 Jan 2026 21:53:39 GMT  
		Size: 19.0 KB (18970 bytes)  
		MIME: application/vnd.in-toto+json
