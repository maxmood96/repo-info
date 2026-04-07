## `dart:stable`

```console
$ docker pull dart@sha256:fd65b23467d84e6470e8050753b976f31229571b79c373b807262d4967aff12b
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
$ docker pull dart@sha256:35f2263aa2c5cfadfd859a5d5fd505f7535561699cb370587ba127d7d7587a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307079619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7806667ee92f61b6ffc726aac6e5e96405c1e70b7face503fcc8ded89875225c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:50:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 07 Apr 2026 01:50:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 07 Apr 2026 01:50:54 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:50:54 GMT
WORKDIR /root
# Tue, 07 Apr 2026 01:51:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8ea6af187f80abf456a2b44b76cdd0f6399572f3e73d4fa571b34de4f1527a`  
		Last Modified: Tue, 07 Apr 2026 01:51:40 GMT  
		Size: 42.5 MB (42502211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e9998d4309937637f7f19723bb7571a6b611998deb8cebd321110c5befb47e`  
		Last Modified: Tue, 07 Apr 2026 01:51:36 GMT  
		Size: 1.9 MB (1869562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d8ed8d741f505bdb34183c1f290b0e624a263edd9afa6b5ccc9f07e483eeb2`  
		Last Modified: Tue, 07 Apr 2026 01:51:45 GMT  
		Size: 232.9 MB (232932174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:3a7c5cedd08b7a8fa8d03073541cd73777dee3e30c9097529a35d7cee9090f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7999d6ddd6dcc5ea4da0ebc79d813bad7b4ed286baf7dfe2e17e0e73b73939fe`

```dockerfile
```

-	Layers:
	-	`sha256:0323b010951b35b4c9a6c461714689ec63dbd938993673449ca1a844aec7f365`  
		Last Modified: Tue, 07 Apr 2026 01:51:36 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:04f4d20b9ef7635dc53a0016b9bbe96e486468428fe54255c27c4b1f1c3d137d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222900756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d748ef573d7264bfc5061ad66df55b00ea9d8a9c756c50c2f3140a11b57bb720`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:05:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:05:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 07 Apr 2026 02:05:10 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 07 Apr 2026 02:05:10 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:05:10 GMT
WORKDIR /root
# Tue, 07 Apr 2026 02:05:19 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3813bffbab6ce7ed35295f369c4fbc3e661e75723d2b754df7de06d2204470`  
		Last Modified: Tue, 07 Apr 2026 02:05:39 GMT  
		Size: 37.5 MB (37496036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a8db82044b33c2d759e59749c16f6a5a71a962490a3eee45b4c350cf5824b0`  
		Last Modified: Tue, 07 Apr 2026 02:05:38 GMT  
		Size: 1.3 MB (1273170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287e9059d80fd200880c8ceccaed623e71eb9f4ee32b8f8b3ee9b19b2cb3e503`  
		Last Modified: Tue, 07 Apr 2026 02:05:43 GMT  
		Size: 157.9 MB (157921865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:a55b457179d1e9f4d5807f9e2b5e8e78e80cabda614d848ec6836f01f58c2bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d4ce50f20476a52e65f1acf795c7d6aaec6d3e235765019cc359f7a8cdc226`

```dockerfile
```

-	Layers:
	-	`sha256:12c9c6f1d369cbd8d27ed892eee5dfe5b626835ea1f2dbe2cb7df06a8e48bbbd`  
		Last Modified: Tue, 07 Apr 2026 02:05:37 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0ce3937e059430573faa610b86fb10e91d02db0aef7affa1cc4db3a13ec4949e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305420418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750f52019ac069789d36b8272aa82f430f98452e1b504b5ad647f185281971fa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:54:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:54:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 07 Apr 2026 01:54:08 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 07 Apr 2026 01:54:08 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:54:08 GMT
WORKDIR /root
# Tue, 07 Apr 2026 01:54:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7619af44f8259e73b23839f43301382c840f467ddd80f8394b971e622c7f5925`  
		Last Modified: Tue, 07 Apr 2026 01:54:49 GMT  
		Size: 42.3 MB (42281561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bae84fccad4f5636115eae45e4ad1b856f21a5afec6073c63170393342c90cf`  
		Last Modified: Tue, 07 Apr 2026 01:54:47 GMT  
		Size: 1.6 MB (1564344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c17af3c954825d486ea376e6abbbbeccbfe06c3e3c72ea5bad1f7e602cdc113`  
		Last Modified: Tue, 07 Apr 2026 01:54:53 GMT  
		Size: 231.4 MB (231435930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:6f06be64c04ff8785936248caebcc0f565ea1ef368253680248bf5bfdd8e3264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfab3968b2b3718beef18bf85709122aa0fdc9d24d9e924a098e2dd883cb554`

```dockerfile
```

-	Layers:
	-	`sha256:9ec1ce2d138123431dfbad37e11c1337cb223472337e066c3303f8f3f7480b2d`  
		Last Modified: Tue, 07 Apr 2026 01:54:47 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; riscv64

```console
$ docker pull dart@sha256:96f8a7981d1fc5b22bd3ca603cbe0b9f17f5a19f39ba6adaf4f5e00931073532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251889122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6365367086bf148b09961e8763f109afb57bae8c607404bd229eabfd6dcbc593`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Wed, 18 Mar 2026 05:15:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 05:15:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 18 Mar 2026 05:15:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 18 Mar 2026 05:15:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Mar 2026 05:15:18 GMT
WORKDIR /root
# Wed, 18 Mar 2026 05:16:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0b5164900a4737bd8c71921f9d6095f2a9499d5081755c56a4aa46d8f37e9865`  
		Last Modified: Mon, 16 Mar 2026 22:10:41 GMT  
		Size: 28.3 MB (28275636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3d0cb338811383f3845e2b916917eb9bbb6af7f87784648cde5676046b45a4`  
		Last Modified: Wed, 18 Mar 2026 05:20:12 GMT  
		Size: 41.6 MB (41565211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6e3f443f1b8babb17b5b44fd2783e0b4bdd466c47db8d14dc58861b38d305b`  
		Last Modified: Wed, 18 Mar 2026 05:19:59 GMT  
		Size: 1.6 MB (1564391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f79c44439c2536795fe00d4fc5458942053a61fa2ec70cef1745812b0ec532a`  
		Last Modified: Wed, 18 Mar 2026 05:20:32 GMT  
		Size: 180.5 MB (180483852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:fdc7d4a77dca7f54f1ae9e92a72d6c8afb41c9c2d66ccec60f05ffe542d69ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ff5ff29409fa550cc17dac73648359060792a9be2934443f27f2492d33d45a`

```dockerfile
```

-	Layers:
	-	`sha256:c516f0d2eb7f69c923386daf77af9fbb7d33b8dfe9acb3608b5506b521d456d9`  
		Last Modified: Wed, 18 Mar 2026 05:19:58 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json
