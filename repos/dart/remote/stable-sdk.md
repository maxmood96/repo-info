## `dart:stable-sdk`

```console
$ docker pull dart@sha256:6a68298156648d3418b7036b4d83a355172e3bdaeb151bbe12af54a25fb3a9fd
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
$ docker pull dart@sha256:2655200cb3db78eb59f9d6647b0371e0327a53687bbbf2961c46de18b448371a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287265401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94ec1d4e40f74358c788cd8f92f45eb80aed0e4de0fc81e5e1da417d4fe269d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 17:45:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 17:45:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Dec 2025 17:45:39 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Dec 2025 17:45:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 17:45:39 GMT
WORKDIR /root
# Tue, 09 Dec 2025 17:45:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=60a9a34eb1165d331d776dc89fb4fd43b9d8bdaf2ca137c1fdcf98d6c89abeec;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2dd412046e8d9fbe429c6fb5f1c042b27f081720c1f1e36a25cc367b7bbe7c52;             SDK_ARCH="arm";;         arm64)             DART_SHA256=828faa614fc2dfcc0d0b44ec646f95d69433124ce0c81a546e75ddd8a5f9a4fa;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1d120852e8406b0b68e42b5494e86c7896e82149018f0478ea956e6803a12c8e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed55b826326c4b293be5821f11363a0a3da8aee3fbf39b904886890115973ac`  
		Last Modified: Tue, 09 Dec 2025 17:46:41 GMT  
		Size: 42.5 MB (42493971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23087ceb8e17b078490cbea2c7bce1d583e547895fdc172551c55581f6d7cbff`  
		Last Modified: Tue, 09 Dec 2025 17:46:37 GMT  
		Size: 1.9 MB (1873622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0b08f0c063ce80e7a600e6425d5b71fb1b62853fb4352bef81f3911d86c86d`  
		Last Modified: Tue, 09 Dec 2025 17:46:43 GMT  
		Size: 213.1 MB (213121280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:f5e7c2db49370425a9b368924a1bc255c56f1661ba9c70968be44a233cb917f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e81eb4e95bff8eb56bcc95d8f732ff0535664b3835f7b06b916525fb72b3224`

```dockerfile
```

-	Layers:
	-	`sha256:a47d9c6697180d07d2f5c35f8aa83448e61714366d1dba15cf7fb3920898475a`  
		Last Modified: Tue, 09 Dec 2025 18:53:24 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:d2754cf80cd31b703bb6b9e115e643e55efa06cebd8bea0f9aac03ef48515917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219909964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1176aca5f7edf9c0e97d0cfdb8b05e9b59656795a1ee22dd608877cfb2f88732`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 17:38:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 17:38:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Dec 2025 17:38:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Dec 2025 17:38:23 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 17:38:23 GMT
WORKDIR /root
# Tue, 09 Dec 2025 17:38:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=60a9a34eb1165d331d776dc89fb4fd43b9d8bdaf2ca137c1fdcf98d6c89abeec;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2dd412046e8d9fbe429c6fb5f1c042b27f081720c1f1e36a25cc367b7bbe7c52;             SDK_ARCH="arm";;         arm64)             DART_SHA256=828faa614fc2dfcc0d0b44ec646f95d69433124ce0c81a546e75ddd8a5f9a4fa;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1d120852e8406b0b68e42b5494e86c7896e82149018f0478ea956e6803a12c8e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b8aa906ef8886bc15ffbd72ddf35b19746b72af73d3c7235e452430c7ae3d9`  
		Last Modified: Tue, 09 Dec 2025 17:39:24 GMT  
		Size: 37.5 MB (37498448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827daef17cc6904066d63ed2435088047e58b7a454bc6c2b135edaf1ec2037a2`  
		Last Modified: Tue, 09 Dec 2025 17:39:19 GMT  
		Size: 1.3 MB (1275122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da8e6c5acf9fd27fd5601a52029d3dec4cd5cb7a2e9eb002d36a6d9b97483f8`  
		Last Modified: Tue, 09 Dec 2025 17:39:55 GMT  
		Size: 154.9 MB (154926349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:328ead12e19a9c19bf7714e5c32a223a4dc6f6d604b4a1edb9d9657a4645e8c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb35b6e58a47f1385b6a76429aca04e0178956dd5f8e3ceb212334cbe147fb51`

```dockerfile
```

-	Layers:
	-	`sha256:7282acd1e2ce9409ad6858ba590bf16d1fedcb74ff4538ab27a380f30f65c325`  
		Last Modified: Tue, 09 Dec 2025 18:53:27 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b84599d76ef7a0ca49eba53bb1918df371de4cae70f29b9d97db41612af3219d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286351819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7faaa9926fe7818291f989815c4c9fe5173907adf37a98748d108ce9f1f99aad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 17:43:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 17:43:26 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Dec 2025 17:43:26 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Dec 2025 17:43:26 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 17:43:26 GMT
WORKDIR /root
# Tue, 09 Dec 2025 17:43:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=60a9a34eb1165d331d776dc89fb4fd43b9d8bdaf2ca137c1fdcf98d6c89abeec;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2dd412046e8d9fbe429c6fb5f1c042b27f081720c1f1e36a25cc367b7bbe7c52;             SDK_ARCH="arm";;         arm64)             DART_SHA256=828faa614fc2dfcc0d0b44ec646f95d69433124ce0c81a546e75ddd8a5f9a4fa;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1d120852e8406b0b68e42b5494e86c7896e82149018f0478ea956e6803a12c8e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9834a9f05f93604ebb6234e573b9cda59dfbc9aaab81b20a0d58b5654f58fd11`  
		Last Modified: Tue, 09 Dec 2025 17:44:22 GMT  
		Size: 42.3 MB (42293368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee3932efc80f13a108a3db0d82af4c86d9138369b07f97acc63ecad686edec8`  
		Last Modified: Tue, 09 Dec 2025 17:44:16 GMT  
		Size: 1.6 MB (1566647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72285918e221d120ea679e00afff2cca8233c57f895d77053f02011655fe5b97`  
		Last Modified: Tue, 09 Dec 2025 17:44:24 GMT  
		Size: 212.4 MB (212353144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:3bd549247e5abb599532e51f5ca4ea98b71616e6ae8ebde76a9c338c00c1ddde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b4cb52d97b66fedc1a98492703412eb8dfe44f4e0554fb74f35594ab749913`

```dockerfile
```

-	Layers:
	-	`sha256:5d5278c2ee852f3ee99abebd271a80100e5d147fc02e3ae043baff5be89b1edf`  
		Last Modified: Tue, 09 Dec 2025 18:53:31 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:ca2e682d07ac57d02e0dda00444fe59b57672fcb42fbd6782df5fda63eacff63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232965995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55e9f87a7ee15b1ac6a02c3f8e09054342da93f74fc64ff9fe90e8f43ea3877`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 18:21:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 18:21:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 18:21:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 18:21:05 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 18:21:05 GMT
WORKDIR /root
# Tue, 02 Dec 2025 18:21:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d187aa75d6411bfc9c015781547398506ff8a5d8e0c4ee5c89cba4597dca7658`  
		Last Modified: Tue, 02 Dec 2025 18:26:43 GMT  
		Size: 41.6 MB (41560771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1041beabf784b9a8a14f47ab8166f4c0734faf36f7141b1c5273529ee215bb06`  
		Last Modified: Tue, 02 Dec 2025 18:26:40 GMT  
		Size: 1.6 MB (1567071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d30c1df1fdda02922e7a0ffdd4a3481728a7b1db6fc160dc082a2d48f343b13`  
		Last Modified: Tue, 02 Dec 2025 21:54:07 GMT  
		Size: 161.6 MB (161564995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:409895074372ea1efcccec2f8f04996c052225c55cf490471d1572fd2aa334e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16ea2ecf25712c5b092186fcfa862d382097777b9f55cb66dab6c1ea6c792b6`

```dockerfile
```

-	Layers:
	-	`sha256:1fc85e7d225072d54ab114ef92e8df8e00b681a43cfdcb19f58e8a0d3c44b9e0`  
		Last Modified: Tue, 02 Dec 2025 21:53:22 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json
