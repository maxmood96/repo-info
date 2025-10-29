## `dart:beta`

```console
$ docker pull dart@sha256:2f3ca2d9b2f5e8cdff963d4346240057429c41154a3f4bc64c937c4c4961ae5d
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
$ docker pull dart@sha256:0af8739f0f090490699c92dab18e6832e63f8aee7c8f961334a4119eae25bdda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287259464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f32f25b1e454510c487cd38eef1143e9b4b296b8dcfa4860699a556c11916e1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Tue, 28 Oct 2025 22:25:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Oct 2025 22:25:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 28 Oct 2025 22:25:46 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 28 Oct 2025 22:25:46 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Oct 2025 22:25:46 GMT
WORKDIR /root
# Tue, 28 Oct 2025 22:25:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f34786de7578862d7d8718f1d70c983b90e7ecfaea29599d7826649be7f0efd3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=649d5e6e31f6189ab216214c0f286e6e5eb74c2ed7e0977f9594d9742afdae5e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=868e2f477c4bfc7c894fec2dddd061a4edb12d7b7ac39d2052e83ac9bfce5bf9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b411452a247b672e87477f60e82ede0a9207a289fac9e544b6089e2dc29a8f1c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5781c0ac40b0f1357e1cfc4164a01d9fbfe1824c489ee268d8808af5d38c53d`  
		Last Modified: Tue, 28 Oct 2025 22:26:36 GMT  
		Size: 42.5 MB (42493503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d344e3845e6145d3bcd057a0f28b94a04bda53029941eb6315d3014f0eed19`  
		Last Modified: Tue, 28 Oct 2025 22:26:33 GMT  
		Size: 1.9 MB (1873623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916aef94fde277c060843046ca4d8bdd5041faae464de3b28d7f839c085f64ec`  
		Last Modified: Tue, 28 Oct 2025 23:54:07 GMT  
		Size: 213.1 MB (213114382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:2c42f0e481d8467a3ea2fc1b34b5fc784bf6e21ca10c0a14ecc8f9792c9c4759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64405a621de4b05eabd11c41db005ddb64425c288f2678d6fa1dc72ae4592fa2`

```dockerfile
```

-	Layers:
	-	`sha256:dd8af3d504259b5865fba52115e0d365ea5e99724b8f69e62de4c255dc1603cf`  
		Last Modified: Tue, 28 Oct 2025 23:53:25 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:6529dbbc2fce6376c7d6768e946a093b77ed738d60b0460c9a9c93b6e89db1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219898369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bd55cc3420ddb98ac7a6dac66543b2474a59c61bd83143e548dd8bd7452705`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Tue, 28 Oct 2025 22:25:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Oct 2025 22:25:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 28 Oct 2025 22:25:45 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 28 Oct 2025 22:25:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Oct 2025 22:25:45 GMT
WORKDIR /root
# Tue, 28 Oct 2025 22:25:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f34786de7578862d7d8718f1d70c983b90e7ecfaea29599d7826649be7f0efd3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=649d5e6e31f6189ab216214c0f286e6e5eb74c2ed7e0977f9594d9742afdae5e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=868e2f477c4bfc7c894fec2dddd061a4edb12d7b7ac39d2052e83ac9bfce5bf9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b411452a247b672e87477f60e82ede0a9207a289fac9e544b6089e2dc29a8f1c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae209e09fa6c360792c585f0387e6c5b0041ba800c61a226f19e07b125ba803`  
		Last Modified: Tue, 28 Oct 2025 22:26:24 GMT  
		Size: 37.5 MB (37498608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d96875a73d98a8d1a434d8f24bf2bbbeed942e24731617fc74e5cba920a6a5`  
		Last Modified: Tue, 28 Oct 2025 22:26:22 GMT  
		Size: 1.3 MB (1275119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ee01f6e03f5ec6baa2082c5505c86eafd1065aea17da1ed18b3e90c3a22e85`  
		Last Modified: Tue, 28 Oct 2025 23:53:53 GMT  
		Size: 154.9 MB (154911716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:d0e05f4ff0c733a1f7b353b6b1903142f592c921a89fbe9db471f657c57747f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed2f29e2b1962ca389527012e2c74d140f3ee7459e0181a8fef88ae36be588a4`

```dockerfile
```

-	Layers:
	-	`sha256:2f9595d633a10830c15d9944ce758e32ca0a78b1296db280f764d155dc4f92fc`  
		Last Modified: Tue, 28 Oct 2025 23:53:27 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:5a94146bf98409e23561a248975c88d064f5b720cc4099db2387e5211d06d443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286339084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9887d094b4af23b1b792ecaf536485d54f97ce660a4850ea644110c26600053`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Tue, 28 Oct 2025 22:42:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Oct 2025 22:42:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 28 Oct 2025 22:42:44 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 28 Oct 2025 22:42:44 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Oct 2025 22:42:44 GMT
WORKDIR /root
# Tue, 28 Oct 2025 22:42:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f34786de7578862d7d8718f1d70c983b90e7ecfaea29599d7826649be7f0efd3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=649d5e6e31f6189ab216214c0f286e6e5eb74c2ed7e0977f9594d9742afdae5e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=868e2f477c4bfc7c894fec2dddd061a4edb12d7b7ac39d2052e83ac9bfce5bf9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b411452a247b672e87477f60e82ede0a9207a289fac9e544b6089e2dc29a8f1c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c936ec72e3b42040d7546e2220ef63b18fa3ee4f6e9dfff83338e97d076ca3d8`  
		Last Modified: Tue, 28 Oct 2025 22:43:34 GMT  
		Size: 42.3 MB (42293169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967125d8b8c0ba242421201ee7b493e6e45b40e9e150724a004840f6bed2fed6`  
		Last Modified: Tue, 28 Oct 2025 22:43:33 GMT  
		Size: 1.6 MB (1566653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1e4a70be59e636b458900e431b58f81cff6b3de1e42ce16f4d2e7eb3ea6cf9`  
		Last Modified: Tue, 28 Oct 2025 22:45:49 GMT  
		Size: 212.3 MB (212337103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:a99f048a1dfb575468d56afceef594b550d7a6328023ebb20bad0e7eecd48f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369dba964e4a033ab5de12121d14caf237d17fcefb39983858a85f3636a6c591`

```dockerfile
```

-	Layers:
	-	`sha256:34f0bd5425cc53f111a8c25d3f0afbb770d392b3195238a90daf8e34d6271897`  
		Last Modified: Tue, 28 Oct 2025 23:53:30 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:05b4c6aae0a3400ee04d484431c490d1afe77bf23b999d4fa55737dd0805470d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232962711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76fa70fae02db8c1a7c9beb26aa8444bf951d0918bdf4314fd5fef418cff8855`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 29 Oct 2025 16:10:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Oct 2025 16:10:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 29 Oct 2025 16:10:43 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 29 Oct 2025 16:10:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Oct 2025 16:10:43 GMT
WORKDIR /root
# Wed, 29 Oct 2025 16:11:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f34786de7578862d7d8718f1d70c983b90e7ecfaea29599d7826649be7f0efd3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=649d5e6e31f6189ab216214c0f286e6e5eb74c2ed7e0977f9594d9742afdae5e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=868e2f477c4bfc7c894fec2dddd061a4edb12d7b7ac39d2052e83ac9bfce5bf9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b411452a247b672e87477f60e82ede0a9207a289fac9e544b6089e2dc29a8f1c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a506f531a9b378b37a57e69ce88af552bafd4f8861debc3cd60759cc0ce24b`  
		Last Modified: Wed, 29 Oct 2025 16:15:46 GMT  
		Size: 41.6 MB (41560624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061570a1fc4dd384af969a49f50fbaa0fdeccf08dfd02e2e5ba2a45039aa23bc`  
		Last Modified: Wed, 29 Oct 2025 16:15:41 GMT  
		Size: 1.6 MB (1567071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da4cdfd96c6e003bf90afc1efa87426ad5e5bc5e5f29044a223762914495bc7`  
		Last Modified: Wed, 29 Oct 2025 17:53:57 GMT  
		Size: 161.6 MB (161559334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:b2a28b6768da7d5db12dd0d4454c8fee4b8753f0dd1fa94aa98283fc68595f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e9724afdeec2f2053bd463a147e902eec2506acd108b13cbef298382c7a634`

```dockerfile
```

-	Layers:
	-	`sha256:da2f1a18510427cb052371790e2df0d2f270b32b723b61166655135fac3d6911`  
		Last Modified: Wed, 29 Oct 2025 17:53:24 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json
