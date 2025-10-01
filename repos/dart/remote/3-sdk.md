## `dart:3-sdk`

```console
$ docker pull dart@sha256:c3bdc5f54a8949d78545011438d1917cb620765e3944894f5e147f93c37ca20a
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
$ docker pull dart@sha256:6371965c88d28b9cca8715a0dcea4879c1b6d55af8c616371eb7951f25a4a449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298340173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee36c77f005ec037f45653cef74b866a43599c3a26543c711c15d883d0f1b3e7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 01 Oct 2025 11:53:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Oct 2025 11:53:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 01 Oct 2025 11:53:58 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Oct 2025 11:53:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Oct 2025 11:53:58 GMT
WORKDIR /root
# Wed, 01 Oct 2025 11:53:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8401b8f51780b5ae1bd97f2bd5eb5e630710042693ac7d0be1019993685808e`  
		Last Modified: Wed, 01 Oct 2025 18:58:01 GMT  
		Size: 45.4 MB (45442158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed4bd23c50b831790efa0f7acd30322d9ae2e0eda448c158d03f065385a7824`  
		Last Modified: Wed, 01 Oct 2025 18:57:58 GMT  
		Size: 1.9 MB (1873617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f64e246cdc5346e7599211b1bdf8e397f9d22866e20f724818a378a3aaf6cfa`  
		Last Modified: Wed, 01 Oct 2025 20:09:54 GMT  
		Size: 221.2 MB (221246600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:f94de84f58f35822c8babb8ab4dcddbd8a91d665585d79ff575f57c5c1d67f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac325e8caa63b92033b0e73438511a40bd937cc6e0ce8aa2e7225730119dc223`

```dockerfile
```

-	Layers:
	-	`sha256:412edf13cd97d42765a0935ca10bc9d3d65b83c16296591642e7249ad6aee1db`  
		Last Modified: Wed, 01 Oct 2025 20:53:24 GMT  
		Size: 20.6 KB (20649 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:af78a1bac04d31d52a6596388d31daea7d66de37c0f5d2b802a6fa366ff00221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222983775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd21bbef1ab73104e2e43a1c1787d0aaae4f39c2c820aca6807bfab5606a053f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Wed, 01 Oct 2025 11:53:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Oct 2025 11:53:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 01 Oct 2025 11:53:58 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Oct 2025 11:53:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Oct 2025 11:53:58 GMT
WORKDIR /root
# Wed, 01 Oct 2025 11:53:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fea7674366d6acc226b723506267ac515f777497fc37e8bc12f8d6cf6b9045`  
		Last Modified: Wed, 01 Oct 2025 17:48:02 GMT  
		Size: 39.7 MB (39690800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75de6f2406d936cac50a98cd1e00689c0f18d1dd380fc1f531a095b37e73a574`  
		Last Modified: Wed, 01 Oct 2025 17:47:55 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9785f0509ccf15cb6b7a1ab1b68b45c85feafa85ce70f5448d407269320101`  
		Last Modified: Wed, 01 Oct 2025 17:48:07 GMT  
		Size: 155.8 MB (155805072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4092668b80ec89f3e2c0b7bacd3f9d640468403dc5453d6e28128579bbf41431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a9ea224c14b37fd92d9728f458749e7e6a7a473b6d26fd70863ab82115836a`

```dockerfile
```

-	Layers:
	-	`sha256:018d2307b291ab4e9f54d7460158e2eced4f02f7cd9af7da82a60874340b6f6b`  
		Last Modified: Wed, 01 Oct 2025 20:53:27 GMT  
		Size: 20.8 KB (20804 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4854c28d2120ec154c2e1263204bfb36f50b70f784b96f5ced52abbb0598112a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (298002852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b779659b9f3d30ced87e82ff60a512e5b0afd19483c7fff2872fbb12131710`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 01 Oct 2025 11:53:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Oct 2025 11:53:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 01 Oct 2025 11:53:58 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Oct 2025 11:53:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Oct 2025 11:53:58 GMT
WORKDIR /root
# Wed, 01 Oct 2025 11:53:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbf50de0fbd892d8179d4c5b1c5cd66e5c2d03e56b18ad2080136acd500ddce`  
		Last Modified: Wed, 01 Oct 2025 17:44:53 GMT  
		Size: 45.6 MB (45599833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26f7617d10c0247876770d45c3ea4a56a5fbcb7fee0eda28bed7e9e88bafc68`  
		Last Modified: Wed, 01 Oct 2025 17:44:49 GMT  
		Size: 1.6 MB (1566644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2617e618a0024ee602c3bfbc0340d9e02c242d1f7481be445cb0cdddd77391e8`  
		Last Modified: Wed, 01 Oct 2025 17:45:40 GMT  
		Size: 220.7 MB (220695501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:d0ca64c2348a52406443936b679ca2f11435c6bea247aa046eb2348fe49fbf0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d886da51908b66a9814a9d405b11e11c57263d8ed32b71bc518d61f786fc45`

```dockerfile
```

-	Layers:
	-	`sha256:0355a32bce1b56abbb4639806e2a109edfc4d53b918f2eb2ea83951b6ed5c786`  
		Last Modified: Wed, 01 Oct 2025 20:53:30 GMT  
		Size: 20.9 KB (20855 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:487a4f03ec06d3e92ae6147293a518ac8258356845650b12d91f2cd56005d8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232354694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94270a625817439c222b7d328a888f8495bd875ac3995e2f2e7e7e223d09743`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487bade7c1f2c6d318deefc56dcd2f3b57c9e9b8edcb9c7acff0685b6dd45f47`  
		Last Modified: Fri, 12 Sep 2025 02:30:59 GMT  
		Size: 41.6 MB (41553204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab7da32ffd5eb9e4d0f4b80406da83fc8883e5c7e25ed26da2c19101b8f4e4d`  
		Last Modified: Fri, 12 Sep 2025 02:30:51 GMT  
		Size: 1.6 MB (1567061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefacbbd56550208f8ee9a29268582b03e59be47f3e902e45f72d6784c9e5af6`  
		Last Modified: Fri, 12 Sep 2025 03:10:47 GMT  
		Size: 161.0 MB (160963025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:144ed8803a2ed4e7691a1eac4a9cd4a369b567ed89b2d0482b19ffe82f3b71a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1741de95e4efdd949c439e3333bacccc5293256558fadcb9b32e9981df429831`

```dockerfile
```

-	Layers:
	-	`sha256:7191e36c55b23642fdbf49bcb46792cb0aafb84fb02b76e3b05e0b096603f046`  
		Last Modified: Fri, 12 Sep 2025 05:53:23 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json
