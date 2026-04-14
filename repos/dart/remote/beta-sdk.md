## `dart:beta-sdk`

```console
$ docker pull dart@sha256:7dbacb8b21ad711e93422bcd338a969585d9a09a7f0e8201f32c50529e56d7ad
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
$ docker pull dart@sha256:af59bbf002c5c66bd43f4dc6fdc612955a1282b565be072ab90da1cce9a03b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.9 MB (313901612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b72fba9b8aac4e9232bdd8525487fef0a75f0092fba51c6d0fe9e209ba0714aa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 14 Apr 2026 18:12:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 18:12:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Apr 2026 18:12:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Apr 2026 18:12:54 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 18:12:54 GMT
WORKDIR /root
# Tue, 14 Apr 2026 18:13:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8471f7632d779ccee562d1a1b44c0eb771b3ad9a7f6b06fd3f82b6206672025d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=357763ff37d605689823e6c2b46c4c96a22c922514c82d57ca598647d04534eb;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e5cd9cc0b45a9ddf2293ad24043db168f3f67ca788387166fc10cb8335469769;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=fe1efce6424f34f4808d662d23ba4f24068c1de11199d37f498435904096b977;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af10c9d0bb15e104d7aaab936f0aa2e73d4e5a9e1d0cc0601eb4036d317fe3a`  
		Last Modified: Tue, 14 Apr 2026 18:13:35 GMT  
		Size: 45.5 MB (45466232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e6ef6f0b3fbf27e77851fc9f1d59328b00772867158df55e5b5a1b52b77ee4`  
		Last Modified: Tue, 14 Apr 2026 18:13:32 GMT  
		Size: 1.9 MB (1869566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a25552b67c3c49b2e7e490d7dbce1d55b4ba1d89c8e1018cd17fdfdcc6bc84`  
		Last Modified: Tue, 14 Apr 2026 18:13:38 GMT  
		Size: 236.8 MB (236790142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:85ec75b822fb836cdcf1a97ae411821421d8f5feb4c98e2caae0ad2c99b2d2a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48a143c2cb1a6596b6a9bbfec67b0bfd8e22f4f9b5e6e463e02a069aee84180`

```dockerfile
```

-	Layers:
	-	`sha256:904ce4040db937b90176295da4824b9e627acb67bcb01bf15a71a85517208064`  
		Last Modified: Tue, 14 Apr 2026 18:13:32 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:a59fec9820f5b261b10ef0b5a0969c889f48c6533817f6b0dd209c5b62516d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228283366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5fa8962641a512b3443f049d71250dd72c154b1fc9f1111ce32947c9b9da615`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 14 Apr 2026 18:12:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 18:12:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Apr 2026 18:12:46 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Apr 2026 18:12:46 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 18:12:46 GMT
WORKDIR /root
# Tue, 14 Apr 2026 18:12:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8471f7632d779ccee562d1a1b44c0eb771b3ad9a7f6b06fd3f82b6206672025d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=357763ff37d605689823e6c2b46c4c96a22c922514c82d57ca598647d04534eb;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e5cd9cc0b45a9ddf2293ad24043db168f3f67ca788387166fc10cb8335469769;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=fe1efce6424f34f4808d662d23ba4f24068c1de11199d37f498435904096b977;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4073b5e2104a9a20fc9d83ea76a6699c52926e848d491088256a8710adc1017a`  
		Last Modified: Tue, 14 Apr 2026 18:13:17 GMT  
		Size: 39.7 MB (39713157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b693afa86126730bac0167742f9ceff1b1589bdbd7e686ceb1958be00122d0f3`  
		Last Modified: Tue, 14 Apr 2026 18:13:15 GMT  
		Size: 1.3 MB (1273162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5fc67c2d1bc4c08ad7e5dad85f8058e2ce7b976ffb7f9a5710a205100cd219`  
		Last Modified: Tue, 14 Apr 2026 18:13:19 GMT  
		Size: 161.1 MB (161087362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:00683a2000f992970cee74a32747091779087df38d66419e28a5c4e180f166ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98b4bd8b9d8e6b90167f8af5c822989e7580081b69440c664390b98d9ee6458`

```dockerfile
```

-	Layers:
	-	`sha256:64a3c91ab853ba31c50755b93919abc03cf029751815fedb8586fdec45b6ff85`  
		Last Modified: Tue, 14 Apr 2026 18:13:15 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4ef05f5f9b7912d4314c71e200fab6c42526263d2381889d8e723a84ac660dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312712203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:106b200274fb44e5ef779604ec32f249db823bc92f88a07e16b8702e33681cb7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 14 Apr 2026 18:12:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 18:12:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Apr 2026 18:12:55 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Apr 2026 18:12:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 18:12:55 GMT
WORKDIR /root
# Tue, 14 Apr 2026 18:13:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8471f7632d779ccee562d1a1b44c0eb771b3ad9a7f6b06fd3f82b6206672025d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=357763ff37d605689823e6c2b46c4c96a22c922514c82d57ca598647d04534eb;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e5cd9cc0b45a9ddf2293ad24043db168f3f67ca788387166fc10cb8335469769;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=fe1efce6424f34f4808d662d23ba4f24068c1de11199d37f498435904096b977;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd834a05fa37011dc853b8c37e472424519fe3966725d05b5bbef749e85988ce`  
		Last Modified: Tue, 14 Apr 2026 18:13:40 GMT  
		Size: 45.6 MB (45615845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4885afdc69e1f1f5d95ed90d3f1299f4e228e228b9b3879ec35683be05d51d4d`  
		Last Modified: Tue, 14 Apr 2026 18:13:38 GMT  
		Size: 1.6 MB (1564342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74a1c217735411b500842d720f8cd46e5a15292c563c4c07cb96543f4c3070b`  
		Last Modified: Tue, 14 Apr 2026 18:13:44 GMT  
		Size: 235.4 MB (235393433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:d8de572f6c5f73834fc0d242d60a8ab14983ada52fd468e46e479630f112949e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2fd664029a3750c2f11bc2526c463600c11afe1e1a5edfb9f6564bcfd0f6c5`

```dockerfile
```

-	Layers:
	-	`sha256:c66e0f73c35fc9d01e9087aeeffaa5d0afabb186958a080900fbd191779d0d98`  
		Last Modified: Tue, 14 Apr 2026 18:13:38 GMT  
		Size: 19.1 KB (19056 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:64304bb2e32f4a24a51a5b76b0f55c950af4842ede5d8c581150a4d2a9159588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250932578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457b7bf0338bd11896b58ec6b45020a1be8e7b805b079a9a768b9a7980d56769`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 14 Apr 2026 18:32:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 18:32:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Apr 2026 18:32:55 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Apr 2026 18:32:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 18:32:55 GMT
WORKDIR /root
# Tue, 14 Apr 2026 18:33:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8471f7632d779ccee562d1a1b44c0eb771b3ad9a7f6b06fd3f82b6206672025d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=357763ff37d605689823e6c2b46c4c96a22c922514c82d57ca598647d04534eb;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e5cd9cc0b45a9ddf2293ad24043db168f3f67ca788387166fc10cb8335469769;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=fe1efce6424f34f4808d662d23ba4f24068c1de11199d37f498435904096b977;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65e322066010d8c2bfd5672d2798420098b528e62c37bfa4953893b3f9d8f73`  
		Last Modified: Tue, 14 Apr 2026 18:37:54 GMT  
		Size: 44.2 MB (44183471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c4c4f2a369fee269da9daa3a87f92d999dec23582a6ef0d154b47095b7d5da`  
		Last Modified: Tue, 14 Apr 2026 18:37:41 GMT  
		Size: 1.6 MB (1564397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8990ae6707f67e5de448b6a4de531513b9a7fd17de7512841c82ac1d958573`  
		Last Modified: Tue, 14 Apr 2026 18:38:14 GMT  
		Size: 176.9 MB (176908900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a4484f54e98d6101798b51cd983d954c665b65065ecbf9341714e4bd37890e73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb9b13c7de85a7fca1e6706b69024ffe3962afbe40740bc545c4f02954a6b7e`

```dockerfile
```

-	Layers:
	-	`sha256:5f74d4b07fb696ebba5ab8ab0fb6d183022faabac2d332ff9d092c3f6dda1644`  
		Last Modified: Tue, 14 Apr 2026 18:37:41 GMT  
		Size: 19.0 KB (18970 bytes)  
		MIME: application/vnd.in-toto+json
