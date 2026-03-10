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
$ docker pull dart@sha256:4fa392688a1d8d122df58e791bb26c512732b9da69a3cb93686f18359768007a
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
$ docker pull dart@sha256:fdbce01fa8eec7bb2822267e0ed775d08ce93d3c1e60282e8c253962424ab4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307072943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f879955ebe22e08effaed6fb6a8f41a81457fc17f028cc451a727eff5341cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 17:27:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 17:27:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 17:27:22 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 17:27:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 17:27:22 GMT
WORKDIR /root
# Tue, 10 Mar 2026 17:27:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebaecf214b547a6eda20ae95caf4304a5e54511b745bd713465e48929ce00b9`  
		Last Modified: Tue, 10 Mar 2026 17:28:02 GMT  
		Size: 42.5 MB (42492259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbd30f011011b8c2b7951eec0bcd9e2b825ea1861dd5a084202b4c38a2c452f`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 1.9 MB (1870165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c87d3eb32792c781e11ede467bc263de71e2bd74dadba1e51c3376c0d17a916`  
		Last Modified: Tue, 10 Mar 2026 17:28:05 GMT  
		Size: 232.9 MB (232931855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:58581453812e031801ddfc96c8345de01611cfdf2941c8592691c75f817d91a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2335bd3715c8c0d4279fa706a4758531977406a2939f71265494982df7333b`

```dockerfile
```

-	Layers:
	-	`sha256:8f8329fe3cc90fe89b9b69af2f805e93f818fd0a0e86b86968b5b24e2e436c32`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:a45bbff844d3b258518f851b89a07be1eda97e2181357ebe21e2690452a71541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222903412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88971476d67c33dce48662e0f31c2c2d0b26528593accb753f9718922430c82`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 18:01:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 18:01:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 18:01:07 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 18:01:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 18:01:07 GMT
WORKDIR /root
# Tue, 10 Mar 2026 18:01:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1939b75bceac29b04b5c1bb3785f4216aa28ce925e1d4a2e58a709ab8bcd23c2`  
		Last Modified: Tue, 10 Mar 2026 18:01:38 GMT  
		Size: 37.5 MB (37494608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd00857f051f4ba385f8094859364b70743cefeb9f20e140644ec0f587e3c7c`  
		Last Modified: Tue, 10 Mar 2026 18:01:36 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95990048096302ee3ecf1ba4cbed0ee0d5b8f61fef1fa1c5806b1438a88a2467`  
		Last Modified: Tue, 10 Mar 2026 18:01:40 GMT  
		Size: 157.9 MB (157921874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:1f93484d6ebc0c4a4ec84e0141f7de6d63bd7b4eaa8c593b0c69fac8c9794c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2dd2a1d7f7bcc145efccdab1dc09540c0e44ad4bfb01d9ad15fb428ce01de41`

```dockerfile
```

-	Layers:
	-	`sha256:71f143846e3cb7bb8a517a810fd9e77b3e2e98571190593b9f7493ef4242d0f5`  
		Last Modified: Tue, 10 Mar 2026 18:01:36 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0a9028f3593f5f6ec72eed477d158bcc4af54ccfe84792097894c3c0ca130bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305432011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9316303ea5cedd9dea99cfa15b11f310b646e6dd73ca9955a8252b21bd1936`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 17:27:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 17:27:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 17:27:21 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 17:27:21 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 17:27:21 GMT
WORKDIR /root
# Tue, 10 Mar 2026 17:27:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a3338f6e2aecfc8130b13ef69938e83589c18b2dca07ceab488685b5d6d14e`  
		Last Modified: Tue, 10 Mar 2026 17:28:02 GMT  
		Size: 42.3 MB (42291774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7229b6a4dd4f0a0478c7caf635e78856040c6f0500e1272bab9ccb7a425466b8`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 1.6 MB (1564520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b565de8325d2f94cca17e82b49f893ce4e9101988c327a10a6c488dadfbb8a2a`  
		Last Modified: Tue, 10 Mar 2026 17:28:06 GMT  
		Size: 231.4 MB (231435587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:eab5fc1888558d46ea75a039426ec9da378b199f20f430e2ca8d1422b635b20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4be896671db4ed16ec0ac70ab95f211f84eb86e3603740446ea12244a63ea`

```dockerfile
```

-	Layers:
	-	`sha256:b068bffec839c81d72f042e72cb74ec732a4b79e335eb2ec0e1194e6d493391e`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; riscv64

```console
$ docker pull dart@sha256:3c50bd3f77c48dabf0745da10733e901a29f50f48375204ffce8b1f8cb3d26b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bbe8353f4bf2c2b74bbfc9d6cd971f71c61c6e854327256bd0e0dfeeb70fb2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:47:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 26 Feb 2026 21:47:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 21:47:17 GMT
WORKDIR /root
# Thu, 26 Feb 2026 21:48:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005b5410669f900e219d8f1011496036e8e069aa48a198a6760555d1e565862`  
		Last Modified: Thu, 26 Feb 2026 21:52:24 GMT  
		Size: 41.6 MB (41560724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b398538cbb3cf53074f900bb3c39189de10e24ab8ad79bc08944898c0008d0`  
		Last Modified: Thu, 26 Feb 2026 21:52:08 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb387d36d548d74ab36773195694e1529dca0153f6b401118c2fad500d6a3be`  
		Last Modified: Thu, 26 Feb 2026 21:52:43 GMT  
		Size: 180.5 MB (180483956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:b2100c2dbdb91555037b5c28a91c8690920255dd893f5c37769d0ed072fce4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2de089cc2eb0543729a77991a9982b076142756be16a0561e5b7d667a651270`

```dockerfile
```

-	Layers:
	-	`sha256:36a836d347e4af15c77b9ab5afc85d735357d7d81cfc4fd67d121798ac3a6a2c`  
		Last Modified: Thu, 26 Feb 2026 21:52:05 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:4fa392688a1d8d122df58e791bb26c512732b9da69a3cb93686f18359768007a
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
$ docker pull dart@sha256:fdbce01fa8eec7bb2822267e0ed775d08ce93d3c1e60282e8c253962424ab4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307072943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f879955ebe22e08effaed6fb6a8f41a81457fc17f028cc451a727eff5341cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 17:27:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 17:27:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 17:27:22 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 17:27:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 17:27:22 GMT
WORKDIR /root
# Tue, 10 Mar 2026 17:27:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebaecf214b547a6eda20ae95caf4304a5e54511b745bd713465e48929ce00b9`  
		Last Modified: Tue, 10 Mar 2026 17:28:02 GMT  
		Size: 42.5 MB (42492259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbd30f011011b8c2b7951eec0bcd9e2b825ea1861dd5a084202b4c38a2c452f`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 1.9 MB (1870165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c87d3eb32792c781e11ede467bc263de71e2bd74dadba1e51c3376c0d17a916`  
		Last Modified: Tue, 10 Mar 2026 17:28:05 GMT  
		Size: 232.9 MB (232931855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:58581453812e031801ddfc96c8345de01611cfdf2941c8592691c75f817d91a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2335bd3715c8c0d4279fa706a4758531977406a2939f71265494982df7333b`

```dockerfile
```

-	Layers:
	-	`sha256:8f8329fe3cc90fe89b9b69af2f805e93f818fd0a0e86b86968b5b24e2e436c32`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:a45bbff844d3b258518f851b89a07be1eda97e2181357ebe21e2690452a71541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222903412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88971476d67c33dce48662e0f31c2c2d0b26528593accb753f9718922430c82`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 18:01:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 18:01:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 18:01:07 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 18:01:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 18:01:07 GMT
WORKDIR /root
# Tue, 10 Mar 2026 18:01:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1939b75bceac29b04b5c1bb3785f4216aa28ce925e1d4a2e58a709ab8bcd23c2`  
		Last Modified: Tue, 10 Mar 2026 18:01:38 GMT  
		Size: 37.5 MB (37494608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd00857f051f4ba385f8094859364b70743cefeb9f20e140644ec0f587e3c7c`  
		Last Modified: Tue, 10 Mar 2026 18:01:36 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95990048096302ee3ecf1ba4cbed0ee0d5b8f61fef1fa1c5806b1438a88a2467`  
		Last Modified: Tue, 10 Mar 2026 18:01:40 GMT  
		Size: 157.9 MB (157921874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1f93484d6ebc0c4a4ec84e0141f7de6d63bd7b4eaa8c593b0c69fac8c9794c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2dd2a1d7f7bcc145efccdab1dc09540c0e44ad4bfb01d9ad15fb428ce01de41`

```dockerfile
```

-	Layers:
	-	`sha256:71f143846e3cb7bb8a517a810fd9e77b3e2e98571190593b9f7493ef4242d0f5`  
		Last Modified: Tue, 10 Mar 2026 18:01:36 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0a9028f3593f5f6ec72eed477d158bcc4af54ccfe84792097894c3c0ca130bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305432011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9316303ea5cedd9dea99cfa15b11f310b646e6dd73ca9955a8252b21bd1936`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 17:27:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 17:27:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 17:27:21 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 17:27:21 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 17:27:21 GMT
WORKDIR /root
# Tue, 10 Mar 2026 17:27:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a3338f6e2aecfc8130b13ef69938e83589c18b2dca07ceab488685b5d6d14e`  
		Last Modified: Tue, 10 Mar 2026 17:28:02 GMT  
		Size: 42.3 MB (42291774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7229b6a4dd4f0a0478c7caf635e78856040c6f0500e1272bab9ccb7a425466b8`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 1.6 MB (1564520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b565de8325d2f94cca17e82b49f893ce4e9101988c327a10a6c488dadfbb8a2a`  
		Last Modified: Tue, 10 Mar 2026 17:28:06 GMT  
		Size: 231.4 MB (231435587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:eab5fc1888558d46ea75a039426ec9da378b199f20f430e2ca8d1422b635b20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4be896671db4ed16ec0ac70ab95f211f84eb86e3603740446ea12244a63ea`

```dockerfile
```

-	Layers:
	-	`sha256:b068bffec839c81d72f042e72cb74ec732a4b79e335eb2ec0e1194e6d493391e`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:3c50bd3f77c48dabf0745da10733e901a29f50f48375204ffce8b1f8cb3d26b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bbe8353f4bf2c2b74bbfc9d6cd971f71c61c6e854327256bd0e0dfeeb70fb2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:47:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 26 Feb 2026 21:47:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 21:47:17 GMT
WORKDIR /root
# Thu, 26 Feb 2026 21:48:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005b5410669f900e219d8f1011496036e8e069aa48a198a6760555d1e565862`  
		Last Modified: Thu, 26 Feb 2026 21:52:24 GMT  
		Size: 41.6 MB (41560724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b398538cbb3cf53074f900bb3c39189de10e24ab8ad79bc08944898c0008d0`  
		Last Modified: Thu, 26 Feb 2026 21:52:08 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb387d36d548d74ab36773195694e1529dca0153f6b401118c2fad500d6a3be`  
		Last Modified: Thu, 26 Feb 2026 21:52:43 GMT  
		Size: 180.5 MB (180483956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b2100c2dbdb91555037b5c28a91c8690920255dd893f5c37769d0ed072fce4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2de089cc2eb0543729a77991a9982b076142756be16a0561e5b7d667a651270`

```dockerfile
```

-	Layers:
	-	`sha256:36a836d347e4af15c77b9ab5afc85d735357d7d81cfc4fd67d121798ac3a6a2c`  
		Last Modified: Thu, 26 Feb 2026 21:52:05 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11`

```console
$ docker pull dart@sha256:4fa392688a1d8d122df58e791bb26c512732b9da69a3cb93686f18359768007a
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
$ docker pull dart@sha256:fdbce01fa8eec7bb2822267e0ed775d08ce93d3c1e60282e8c253962424ab4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307072943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f879955ebe22e08effaed6fb6a8f41a81457fc17f028cc451a727eff5341cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 17:27:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 17:27:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 17:27:22 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 17:27:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 17:27:22 GMT
WORKDIR /root
# Tue, 10 Mar 2026 17:27:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebaecf214b547a6eda20ae95caf4304a5e54511b745bd713465e48929ce00b9`  
		Last Modified: Tue, 10 Mar 2026 17:28:02 GMT  
		Size: 42.5 MB (42492259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbd30f011011b8c2b7951eec0bcd9e2b825ea1861dd5a084202b4c38a2c452f`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 1.9 MB (1870165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c87d3eb32792c781e11ede467bc263de71e2bd74dadba1e51c3376c0d17a916`  
		Last Modified: Tue, 10 Mar 2026 17:28:05 GMT  
		Size: 232.9 MB (232931855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:58581453812e031801ddfc96c8345de01611cfdf2941c8592691c75f817d91a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2335bd3715c8c0d4279fa706a4758531977406a2939f71265494982df7333b`

```dockerfile
```

-	Layers:
	-	`sha256:8f8329fe3cc90fe89b9b69af2f805e93f818fd0a0e86b86968b5b24e2e436c32`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11` - linux; arm variant v7

```console
$ docker pull dart@sha256:a45bbff844d3b258518f851b89a07be1eda97e2181357ebe21e2690452a71541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222903412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88971476d67c33dce48662e0f31c2c2d0b26528593accb753f9718922430c82`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 18:01:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 18:01:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 18:01:07 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 18:01:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 18:01:07 GMT
WORKDIR /root
# Tue, 10 Mar 2026 18:01:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1939b75bceac29b04b5c1bb3785f4216aa28ce925e1d4a2e58a709ab8bcd23c2`  
		Last Modified: Tue, 10 Mar 2026 18:01:38 GMT  
		Size: 37.5 MB (37494608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd00857f051f4ba385f8094859364b70743cefeb9f20e140644ec0f587e3c7c`  
		Last Modified: Tue, 10 Mar 2026 18:01:36 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95990048096302ee3ecf1ba4cbed0ee0d5b8f61fef1fa1c5806b1438a88a2467`  
		Last Modified: Tue, 10 Mar 2026 18:01:40 GMT  
		Size: 157.9 MB (157921874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:1f93484d6ebc0c4a4ec84e0141f7de6d63bd7b4eaa8c593b0c69fac8c9794c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2dd2a1d7f7bcc145efccdab1dc09540c0e44ad4bfb01d9ad15fb428ce01de41`

```dockerfile
```

-	Layers:
	-	`sha256:71f143846e3cb7bb8a517a810fd9e77b3e2e98571190593b9f7493ef4242d0f5`  
		Last Modified: Tue, 10 Mar 2026 18:01:36 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0a9028f3593f5f6ec72eed477d158bcc4af54ccfe84792097894c3c0ca130bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305432011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9316303ea5cedd9dea99cfa15b11f310b646e6dd73ca9955a8252b21bd1936`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 17:27:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 17:27:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 17:27:21 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 17:27:21 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 17:27:21 GMT
WORKDIR /root
# Tue, 10 Mar 2026 17:27:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a3338f6e2aecfc8130b13ef69938e83589c18b2dca07ceab488685b5d6d14e`  
		Last Modified: Tue, 10 Mar 2026 17:28:02 GMT  
		Size: 42.3 MB (42291774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7229b6a4dd4f0a0478c7caf635e78856040c6f0500e1272bab9ccb7a425466b8`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 1.6 MB (1564520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b565de8325d2f94cca17e82b49f893ce4e9101988c327a10a6c488dadfbb8a2a`  
		Last Modified: Tue, 10 Mar 2026 17:28:06 GMT  
		Size: 231.4 MB (231435587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:eab5fc1888558d46ea75a039426ec9da378b199f20f430e2ca8d1422b635b20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4be896671db4ed16ec0ac70ab95f211f84eb86e3603740446ea12244a63ea`

```dockerfile
```

-	Layers:
	-	`sha256:b068bffec839c81d72f042e72cb74ec732a4b79e335eb2ec0e1194e6d493391e`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11` - linux; riscv64

```console
$ docker pull dart@sha256:3c50bd3f77c48dabf0745da10733e901a29f50f48375204ffce8b1f8cb3d26b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bbe8353f4bf2c2b74bbfc9d6cd971f71c61c6e854327256bd0e0dfeeb70fb2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:47:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 26 Feb 2026 21:47:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 21:47:17 GMT
WORKDIR /root
# Thu, 26 Feb 2026 21:48:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005b5410669f900e219d8f1011496036e8e069aa48a198a6760555d1e565862`  
		Last Modified: Thu, 26 Feb 2026 21:52:24 GMT  
		Size: 41.6 MB (41560724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b398538cbb3cf53074f900bb3c39189de10e24ab8ad79bc08944898c0008d0`  
		Last Modified: Thu, 26 Feb 2026 21:52:08 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb387d36d548d74ab36773195694e1529dca0153f6b401118c2fad500d6a3be`  
		Last Modified: Thu, 26 Feb 2026 21:52:43 GMT  
		Size: 180.5 MB (180483956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:b2100c2dbdb91555037b5c28a91c8690920255dd893f5c37769d0ed072fce4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2de089cc2eb0543729a77991a9982b076142756be16a0561e5b7d667a651270`

```dockerfile
```

-	Layers:
	-	`sha256:36a836d347e4af15c77b9ab5afc85d735357d7d81cfc4fd67d121798ac3a6a2c`  
		Last Modified: Thu, 26 Feb 2026 21:52:05 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11-sdk`

```console
$ docker pull dart@sha256:4fa392688a1d8d122df58e791bb26c512732b9da69a3cb93686f18359768007a
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
$ docker pull dart@sha256:fdbce01fa8eec7bb2822267e0ed775d08ce93d3c1e60282e8c253962424ab4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307072943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f879955ebe22e08effaed6fb6a8f41a81457fc17f028cc451a727eff5341cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 17:27:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 17:27:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 17:27:22 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 17:27:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 17:27:22 GMT
WORKDIR /root
# Tue, 10 Mar 2026 17:27:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebaecf214b547a6eda20ae95caf4304a5e54511b745bd713465e48929ce00b9`  
		Last Modified: Tue, 10 Mar 2026 17:28:02 GMT  
		Size: 42.5 MB (42492259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbd30f011011b8c2b7951eec0bcd9e2b825ea1861dd5a084202b4c38a2c452f`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 1.9 MB (1870165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c87d3eb32792c781e11ede467bc263de71e2bd74dadba1e51c3376c0d17a916`  
		Last Modified: Tue, 10 Mar 2026 17:28:05 GMT  
		Size: 232.9 MB (232931855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:58581453812e031801ddfc96c8345de01611cfdf2941c8592691c75f817d91a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2335bd3715c8c0d4279fa706a4758531977406a2939f71265494982df7333b`

```dockerfile
```

-	Layers:
	-	`sha256:8f8329fe3cc90fe89b9b69af2f805e93f818fd0a0e86b86968b5b24e2e436c32`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:a45bbff844d3b258518f851b89a07be1eda97e2181357ebe21e2690452a71541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222903412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88971476d67c33dce48662e0f31c2c2d0b26528593accb753f9718922430c82`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 18:01:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 18:01:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 18:01:07 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 18:01:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 18:01:07 GMT
WORKDIR /root
# Tue, 10 Mar 2026 18:01:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1939b75bceac29b04b5c1bb3785f4216aa28ce925e1d4a2e58a709ab8bcd23c2`  
		Last Modified: Tue, 10 Mar 2026 18:01:38 GMT  
		Size: 37.5 MB (37494608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd00857f051f4ba385f8094859364b70743cefeb9f20e140644ec0f587e3c7c`  
		Last Modified: Tue, 10 Mar 2026 18:01:36 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95990048096302ee3ecf1ba4cbed0ee0d5b8f61fef1fa1c5806b1438a88a2467`  
		Last Modified: Tue, 10 Mar 2026 18:01:40 GMT  
		Size: 157.9 MB (157921874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1f93484d6ebc0c4a4ec84e0141f7de6d63bd7b4eaa8c593b0c69fac8c9794c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2dd2a1d7f7bcc145efccdab1dc09540c0e44ad4bfb01d9ad15fb428ce01de41`

```dockerfile
```

-	Layers:
	-	`sha256:71f143846e3cb7bb8a517a810fd9e77b3e2e98571190593b9f7493ef4242d0f5`  
		Last Modified: Tue, 10 Mar 2026 18:01:36 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0a9028f3593f5f6ec72eed477d158bcc4af54ccfe84792097894c3c0ca130bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305432011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9316303ea5cedd9dea99cfa15b11f310b646e6dd73ca9955a8252b21bd1936`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 17:27:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 17:27:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 17:27:21 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 17:27:21 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 17:27:21 GMT
WORKDIR /root
# Tue, 10 Mar 2026 17:27:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a3338f6e2aecfc8130b13ef69938e83589c18b2dca07ceab488685b5d6d14e`  
		Last Modified: Tue, 10 Mar 2026 17:28:02 GMT  
		Size: 42.3 MB (42291774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7229b6a4dd4f0a0478c7caf635e78856040c6f0500e1272bab9ccb7a425466b8`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 1.6 MB (1564520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b565de8325d2f94cca17e82b49f893ce4e9101988c327a10a6c488dadfbb8a2a`  
		Last Modified: Tue, 10 Mar 2026 17:28:06 GMT  
		Size: 231.4 MB (231435587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:eab5fc1888558d46ea75a039426ec9da378b199f20f430e2ca8d1422b635b20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4be896671db4ed16ec0ac70ab95f211f84eb86e3603740446ea12244a63ea`

```dockerfile
```

-	Layers:
	-	`sha256:b068bffec839c81d72f042e72cb74ec732a4b79e335eb2ec0e1194e6d493391e`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:3c50bd3f77c48dabf0745da10733e901a29f50f48375204ffce8b1f8cb3d26b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bbe8353f4bf2c2b74bbfc9d6cd971f71c61c6e854327256bd0e0dfeeb70fb2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:47:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 26 Feb 2026 21:47:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 21:47:17 GMT
WORKDIR /root
# Thu, 26 Feb 2026 21:48:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005b5410669f900e219d8f1011496036e8e069aa48a198a6760555d1e565862`  
		Last Modified: Thu, 26 Feb 2026 21:52:24 GMT  
		Size: 41.6 MB (41560724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b398538cbb3cf53074f900bb3c39189de10e24ab8ad79bc08944898c0008d0`  
		Last Modified: Thu, 26 Feb 2026 21:52:08 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb387d36d548d74ab36773195694e1529dca0153f6b401118c2fad500d6a3be`  
		Last Modified: Thu, 26 Feb 2026 21:52:43 GMT  
		Size: 180.5 MB (180483956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b2100c2dbdb91555037b5c28a91c8690920255dd893f5c37769d0ed072fce4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2de089cc2eb0543729a77991a9982b076142756be16a0561e5b7d667a651270`

```dockerfile
```

-	Layers:
	-	`sha256:36a836d347e4af15c77b9ab5afc85d735357d7d81cfc4fd67d121798ac3a6a2c`  
		Last Modified: Thu, 26 Feb 2026 21:52:05 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.2`

```console
$ docker pull dart@sha256:b0f73636933b6e10b574b3118856cec6c2b3e8074e2ce4229c0838aef66ae203
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.11.2` - linux; amd64

```console
$ docker pull dart@sha256:fdbce01fa8eec7bb2822267e0ed775d08ce93d3c1e60282e8c253962424ab4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307072943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f879955ebe22e08effaed6fb6a8f41a81457fc17f028cc451a727eff5341cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 17:27:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 17:27:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 17:27:22 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 17:27:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 17:27:22 GMT
WORKDIR /root
# Tue, 10 Mar 2026 17:27:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebaecf214b547a6eda20ae95caf4304a5e54511b745bd713465e48929ce00b9`  
		Last Modified: Tue, 10 Mar 2026 17:28:02 GMT  
		Size: 42.5 MB (42492259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbd30f011011b8c2b7951eec0bcd9e2b825ea1861dd5a084202b4c38a2c452f`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 1.9 MB (1870165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c87d3eb32792c781e11ede467bc263de71e2bd74dadba1e51c3376c0d17a916`  
		Last Modified: Tue, 10 Mar 2026 17:28:05 GMT  
		Size: 232.9 MB (232931855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.2` - unknown; unknown

```console
$ docker pull dart@sha256:58581453812e031801ddfc96c8345de01611cfdf2941c8592691c75f817d91a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2335bd3715c8c0d4279fa706a4758531977406a2939f71265494982df7333b`

```dockerfile
```

-	Layers:
	-	`sha256:8f8329fe3cc90fe89b9b69af2f805e93f818fd0a0e86b86968b5b24e2e436c32`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.2` - linux; arm variant v7

```console
$ docker pull dart@sha256:a45bbff844d3b258518f851b89a07be1eda97e2181357ebe21e2690452a71541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222903412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88971476d67c33dce48662e0f31c2c2d0b26528593accb753f9718922430c82`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 18:01:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 18:01:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 18:01:07 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 18:01:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 18:01:07 GMT
WORKDIR /root
# Tue, 10 Mar 2026 18:01:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1939b75bceac29b04b5c1bb3785f4216aa28ce925e1d4a2e58a709ab8bcd23c2`  
		Last Modified: Tue, 10 Mar 2026 18:01:38 GMT  
		Size: 37.5 MB (37494608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd00857f051f4ba385f8094859364b70743cefeb9f20e140644ec0f587e3c7c`  
		Last Modified: Tue, 10 Mar 2026 18:01:36 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95990048096302ee3ecf1ba4cbed0ee0d5b8f61fef1fa1c5806b1438a88a2467`  
		Last Modified: Tue, 10 Mar 2026 18:01:40 GMT  
		Size: 157.9 MB (157921874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.2` - unknown; unknown

```console
$ docker pull dart@sha256:1f93484d6ebc0c4a4ec84e0141f7de6d63bd7b4eaa8c593b0c69fac8c9794c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2dd2a1d7f7bcc145efccdab1dc09540c0e44ad4bfb01d9ad15fb428ce01de41`

```dockerfile
```

-	Layers:
	-	`sha256:71f143846e3cb7bb8a517a810fd9e77b3e2e98571190593b9f7493ef4242d0f5`  
		Last Modified: Tue, 10 Mar 2026 18:01:36 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.2` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0a9028f3593f5f6ec72eed477d158bcc4af54ccfe84792097894c3c0ca130bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305432011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9316303ea5cedd9dea99cfa15b11f310b646e6dd73ca9955a8252b21bd1936`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 17:27:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 17:27:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 17:27:21 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 17:27:21 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 17:27:21 GMT
WORKDIR /root
# Tue, 10 Mar 2026 17:27:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a3338f6e2aecfc8130b13ef69938e83589c18b2dca07ceab488685b5d6d14e`  
		Last Modified: Tue, 10 Mar 2026 17:28:02 GMT  
		Size: 42.3 MB (42291774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7229b6a4dd4f0a0478c7caf635e78856040c6f0500e1272bab9ccb7a425466b8`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 1.6 MB (1564520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b565de8325d2f94cca17e82b49f893ce4e9101988c327a10a6c488dadfbb8a2a`  
		Last Modified: Tue, 10 Mar 2026 17:28:06 GMT  
		Size: 231.4 MB (231435587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.2` - unknown; unknown

```console
$ docker pull dart@sha256:eab5fc1888558d46ea75a039426ec9da378b199f20f430e2ca8d1422b635b20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4be896671db4ed16ec0ac70ab95f211f84eb86e3603740446ea12244a63ea`

```dockerfile
```

-	Layers:
	-	`sha256:b068bffec839c81d72f042e72cb74ec732a4b79e335eb2ec0e1194e6d493391e`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.2-sdk`

```console
$ docker pull dart@sha256:b0f73636933b6e10b574b3118856cec6c2b3e8074e2ce4229c0838aef66ae203
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.11.2-sdk` - linux; amd64

```console
$ docker pull dart@sha256:fdbce01fa8eec7bb2822267e0ed775d08ce93d3c1e60282e8c253962424ab4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307072943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f879955ebe22e08effaed6fb6a8f41a81457fc17f028cc451a727eff5341cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 17:27:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 17:27:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 17:27:22 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 17:27:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 17:27:22 GMT
WORKDIR /root
# Tue, 10 Mar 2026 17:27:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebaecf214b547a6eda20ae95caf4304a5e54511b745bd713465e48929ce00b9`  
		Last Modified: Tue, 10 Mar 2026 17:28:02 GMT  
		Size: 42.5 MB (42492259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbd30f011011b8c2b7951eec0bcd9e2b825ea1861dd5a084202b4c38a2c452f`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 1.9 MB (1870165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c87d3eb32792c781e11ede467bc263de71e2bd74dadba1e51c3376c0d17a916`  
		Last Modified: Tue, 10 Mar 2026 17:28:05 GMT  
		Size: 232.9 MB (232931855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.2-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:58581453812e031801ddfc96c8345de01611cfdf2941c8592691c75f817d91a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2335bd3715c8c0d4279fa706a4758531977406a2939f71265494982df7333b`

```dockerfile
```

-	Layers:
	-	`sha256:8f8329fe3cc90fe89b9b69af2f805e93f818fd0a0e86b86968b5b24e2e436c32`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.2-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:a45bbff844d3b258518f851b89a07be1eda97e2181357ebe21e2690452a71541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222903412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88971476d67c33dce48662e0f31c2c2d0b26528593accb753f9718922430c82`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 18:01:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 18:01:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 18:01:07 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 18:01:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 18:01:07 GMT
WORKDIR /root
# Tue, 10 Mar 2026 18:01:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1939b75bceac29b04b5c1bb3785f4216aa28ce925e1d4a2e58a709ab8bcd23c2`  
		Last Modified: Tue, 10 Mar 2026 18:01:38 GMT  
		Size: 37.5 MB (37494608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd00857f051f4ba385f8094859364b70743cefeb9f20e140644ec0f587e3c7c`  
		Last Modified: Tue, 10 Mar 2026 18:01:36 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95990048096302ee3ecf1ba4cbed0ee0d5b8f61fef1fa1c5806b1438a88a2467`  
		Last Modified: Tue, 10 Mar 2026 18:01:40 GMT  
		Size: 157.9 MB (157921874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.2-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1f93484d6ebc0c4a4ec84e0141f7de6d63bd7b4eaa8c593b0c69fac8c9794c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2dd2a1d7f7bcc145efccdab1dc09540c0e44ad4bfb01d9ad15fb428ce01de41`

```dockerfile
```

-	Layers:
	-	`sha256:71f143846e3cb7bb8a517a810fd9e77b3e2e98571190593b9f7493ef4242d0f5`  
		Last Modified: Tue, 10 Mar 2026 18:01:36 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.2-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0a9028f3593f5f6ec72eed477d158bcc4af54ccfe84792097894c3c0ca130bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305432011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9316303ea5cedd9dea99cfa15b11f310b646e6dd73ca9955a8252b21bd1936`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 17:27:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 17:27:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 17:27:21 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 17:27:21 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 17:27:21 GMT
WORKDIR /root
# Tue, 10 Mar 2026 17:27:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a3338f6e2aecfc8130b13ef69938e83589c18b2dca07ceab488685b5d6d14e`  
		Last Modified: Tue, 10 Mar 2026 17:28:02 GMT  
		Size: 42.3 MB (42291774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7229b6a4dd4f0a0478c7caf635e78856040c6f0500e1272bab9ccb7a425466b8`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 1.6 MB (1564520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b565de8325d2f94cca17e82b49f893ce4e9101988c327a10a6c488dadfbb8a2a`  
		Last Modified: Tue, 10 Mar 2026 17:28:06 GMT  
		Size: 231.4 MB (231435587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.2-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:eab5fc1888558d46ea75a039426ec9da378b199f20f430e2ca8d1422b635b20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4be896671db4ed16ec0ac70ab95f211f84eb86e3603740446ea12244a63ea`

```dockerfile
```

-	Layers:
	-	`sha256:b068bffec839c81d72f042e72cb74ec732a4b79e335eb2ec0e1194e6d493391e`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.12.0-210.1.beta`

```console
$ docker pull dart@sha256:7ca43dc0a97bf5420533955af8081a76fd15c4b6f323d30fee9ef0e837c2da73
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
$ docker pull dart@sha256:1c5c80214dcda5103ce6a2d1ebb369ee3c9f3aa8bce99b034a7b87b952799859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311295869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8250ddf92e72abca3288d3f095cd498aa2fead750b20dc02685aa5d3a9926296`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Fri, 06 Mar 2026 00:21:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 00:21:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 06 Mar 2026 00:21:04 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 06 Mar 2026 00:21:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 00:21:04 GMT
WORKDIR /root
# Fri, 06 Mar 2026 00:21:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ae1380938bad3262dfec743c25edb03489a257cce6214a0e8fc279cd31fbef`  
		Last Modified: Fri, 06 Mar 2026 00:21:46 GMT  
		Size: 42.5 MB (42492345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c381b60c3acba3839fa880b174bcccb173f7f01e16d31b07dc2fa8f02ed841`  
		Last Modified: Fri, 06 Mar 2026 00:21:45 GMT  
		Size: 1.9 MB (1870171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9972a34f550f06085aa60628dcb9ab6bc1e01a0e6caff8c6329962ccb952c30`  
		Last Modified: Fri, 06 Mar 2026 00:21:50 GMT  
		Size: 237.2 MB (237154689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-210.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:d84eb9dd45596cad707b69f6899bf73438c0f21f3dc2d0ca450106a6956591aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc8af74e65dbaa0c022ccdd65843b0cd67662cb0055b81e48a54ab54c124c07`

```dockerfile
```

-	Layers:
	-	`sha256:b10d02ee74400fcc336bd4e99e4edd46cb4a0018ef0f18b5c0bfb153f4e18404`  
		Last Modified: Fri, 06 Mar 2026 00:21:45 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.0-210.1.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:39e05747e040aa04521fe54514ba90522ec2c250c890b2d215b058b53db117b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225635138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45a1a4d83a1ea80478e5286a4368e8e93cf4268519ae923cec47f669b330ae5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Fri, 06 Mar 2026 00:20:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 00:20:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 06 Mar 2026 00:20:48 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 06 Mar 2026 00:20:48 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 00:20:48 GMT
WORKDIR /root
# Fri, 06 Mar 2026 00:20:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43bae8a64ab919bfe317a983a6e223ba905d760574188662362ac17f82fca5a`  
		Last Modified: Fri, 06 Mar 2026 00:21:18 GMT  
		Size: 37.5 MB (37494474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7cd566e4da2372190781a4eb382595d46b7e784c8a1af7de638ab7abb876a`  
		Last Modified: Fri, 06 Mar 2026 00:21:16 GMT  
		Size: 1.3 MB (1273170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baaa18467108c119d6fc8b8b7961886fb61580d0714a0012e16269896cd5859`  
		Last Modified: Fri, 06 Mar 2026 00:21:20 GMT  
		Size: 160.7 MB (160653717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-210.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:7eaefd5e6bcf5b5d442af1bca387a5f7f49c127779ac45b18b03da13a7d986b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb50d3451d4bbff18f7af3e34a1eefda1394950c171a9fbc2c3b1b560277d00c`

```dockerfile
```

-	Layers:
	-	`sha256:4dd5f7c6233b8fed4902c20155338f7cc99237052057b642cd8e1cf5e0b46ae4`  
		Last Modified: Fri, 06 Mar 2026 00:21:16 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.0-210.1.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:1e79efd46afee2b5c12be6200a9547e26fd1e75492b14e2a44fbc549f88f8536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 MB (309723442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72643dbfff39225ae8e46fbafbe481d2c3927ee0bd2a9c57d13614103f3e10f5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Fri, 06 Mar 2026 00:20:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 00:20:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 06 Mar 2026 00:20:56 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 06 Mar 2026 00:20:56 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 00:20:56 GMT
WORKDIR /root
# Fri, 06 Mar 2026 00:21:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68833b8860f3f32f0b393f82d6a208b74aa83d5804a1d9ab4b4ee48a3bd80a7b`  
		Last Modified: Fri, 06 Mar 2026 00:21:40 GMT  
		Size: 42.3 MB (42291717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0a8f75efd4bef95965c7fea5ec957210cfb4f7cfb8ee8870548c2502a88105`  
		Last Modified: Fri, 06 Mar 2026 00:21:38 GMT  
		Size: 1.6 MB (1564523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42318ba95572b11796a1c9d780aa04909d644538cc20ee5cf737262f2c22bfe5`  
		Last Modified: Fri, 06 Mar 2026 00:21:47 GMT  
		Size: 235.7 MB (235727072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-210.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:074d7f80b37076d41ea85ae0a0f4563bdf504bc720e6c1aed0344cf9e23415cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2011b4c902d628294980bc2be5d6a24f4186c8db02fa114f2e2ceb69b6fa868`

```dockerfile
```

-	Layers:
	-	`sha256:5373b3825806b03b920125eae61eaa86952ab43330b19a28b767b2c84cfadc28`  
		Last Modified: Fri, 06 Mar 2026 00:21:38 GMT  
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
$ docker pull dart@sha256:7ca43dc0a97bf5420533955af8081a76fd15c4b6f323d30fee9ef0e837c2da73
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
$ docker pull dart@sha256:1c5c80214dcda5103ce6a2d1ebb369ee3c9f3aa8bce99b034a7b87b952799859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311295869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8250ddf92e72abca3288d3f095cd498aa2fead750b20dc02685aa5d3a9926296`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Fri, 06 Mar 2026 00:21:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 00:21:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 06 Mar 2026 00:21:04 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 06 Mar 2026 00:21:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 00:21:04 GMT
WORKDIR /root
# Fri, 06 Mar 2026 00:21:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ae1380938bad3262dfec743c25edb03489a257cce6214a0e8fc279cd31fbef`  
		Last Modified: Fri, 06 Mar 2026 00:21:46 GMT  
		Size: 42.5 MB (42492345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c381b60c3acba3839fa880b174bcccb173f7f01e16d31b07dc2fa8f02ed841`  
		Last Modified: Fri, 06 Mar 2026 00:21:45 GMT  
		Size: 1.9 MB (1870171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9972a34f550f06085aa60628dcb9ab6bc1e01a0e6caff8c6329962ccb952c30`  
		Last Modified: Fri, 06 Mar 2026 00:21:50 GMT  
		Size: 237.2 MB (237154689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-210.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:d84eb9dd45596cad707b69f6899bf73438c0f21f3dc2d0ca450106a6956591aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc8af74e65dbaa0c022ccdd65843b0cd67662cb0055b81e48a54ab54c124c07`

```dockerfile
```

-	Layers:
	-	`sha256:b10d02ee74400fcc336bd4e99e4edd46cb4a0018ef0f18b5c0bfb153f4e18404`  
		Last Modified: Fri, 06 Mar 2026 00:21:45 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.0-210.1.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:39e05747e040aa04521fe54514ba90522ec2c250c890b2d215b058b53db117b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225635138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45a1a4d83a1ea80478e5286a4368e8e93cf4268519ae923cec47f669b330ae5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Fri, 06 Mar 2026 00:20:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 00:20:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 06 Mar 2026 00:20:48 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 06 Mar 2026 00:20:48 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 00:20:48 GMT
WORKDIR /root
# Fri, 06 Mar 2026 00:20:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43bae8a64ab919bfe317a983a6e223ba905d760574188662362ac17f82fca5a`  
		Last Modified: Fri, 06 Mar 2026 00:21:18 GMT  
		Size: 37.5 MB (37494474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7cd566e4da2372190781a4eb382595d46b7e784c8a1af7de638ab7abb876a`  
		Last Modified: Fri, 06 Mar 2026 00:21:16 GMT  
		Size: 1.3 MB (1273170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baaa18467108c119d6fc8b8b7961886fb61580d0714a0012e16269896cd5859`  
		Last Modified: Fri, 06 Mar 2026 00:21:20 GMT  
		Size: 160.7 MB (160653717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-210.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7eaefd5e6bcf5b5d442af1bca387a5f7f49c127779ac45b18b03da13a7d986b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb50d3451d4bbff18f7af3e34a1eefda1394950c171a9fbc2c3b1b560277d00c`

```dockerfile
```

-	Layers:
	-	`sha256:4dd5f7c6233b8fed4902c20155338f7cc99237052057b642cd8e1cf5e0b46ae4`  
		Last Modified: Fri, 06 Mar 2026 00:21:16 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.0-210.1.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:1e79efd46afee2b5c12be6200a9547e26fd1e75492b14e2a44fbc549f88f8536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 MB (309723442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72643dbfff39225ae8e46fbafbe481d2c3927ee0bd2a9c57d13614103f3e10f5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Fri, 06 Mar 2026 00:20:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 00:20:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 06 Mar 2026 00:20:56 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 06 Mar 2026 00:20:56 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 00:20:56 GMT
WORKDIR /root
# Fri, 06 Mar 2026 00:21:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68833b8860f3f32f0b393f82d6a208b74aa83d5804a1d9ab4b4ee48a3bd80a7b`  
		Last Modified: Fri, 06 Mar 2026 00:21:40 GMT  
		Size: 42.3 MB (42291717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0a8f75efd4bef95965c7fea5ec957210cfb4f7cfb8ee8870548c2502a88105`  
		Last Modified: Fri, 06 Mar 2026 00:21:38 GMT  
		Size: 1.6 MB (1564523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42318ba95572b11796a1c9d780aa04909d644538cc20ee5cf737262f2c22bfe5`  
		Last Modified: Fri, 06 Mar 2026 00:21:47 GMT  
		Size: 235.7 MB (235727072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-210.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:074d7f80b37076d41ea85ae0a0f4563bdf504bc720e6c1aed0344cf9e23415cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2011b4c902d628294980bc2be5d6a24f4186c8db02fa114f2e2ceb69b6fa868`

```dockerfile
```

-	Layers:
	-	`sha256:5373b3825806b03b920125eae61eaa86952ab43330b19a28b767b2c84cfadc28`  
		Last Modified: Fri, 06 Mar 2026 00:21:38 GMT  
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
$ docker pull dart@sha256:7ca43dc0a97bf5420533955af8081a76fd15c4b6f323d30fee9ef0e837c2da73
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
$ docker pull dart@sha256:1c5c80214dcda5103ce6a2d1ebb369ee3c9f3aa8bce99b034a7b87b952799859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311295869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8250ddf92e72abca3288d3f095cd498aa2fead750b20dc02685aa5d3a9926296`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Fri, 06 Mar 2026 00:21:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 00:21:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 06 Mar 2026 00:21:04 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 06 Mar 2026 00:21:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 00:21:04 GMT
WORKDIR /root
# Fri, 06 Mar 2026 00:21:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ae1380938bad3262dfec743c25edb03489a257cce6214a0e8fc279cd31fbef`  
		Last Modified: Fri, 06 Mar 2026 00:21:46 GMT  
		Size: 42.5 MB (42492345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c381b60c3acba3839fa880b174bcccb173f7f01e16d31b07dc2fa8f02ed841`  
		Last Modified: Fri, 06 Mar 2026 00:21:45 GMT  
		Size: 1.9 MB (1870171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9972a34f550f06085aa60628dcb9ab6bc1e01a0e6caff8c6329962ccb952c30`  
		Last Modified: Fri, 06 Mar 2026 00:21:50 GMT  
		Size: 237.2 MB (237154689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:d84eb9dd45596cad707b69f6899bf73438c0f21f3dc2d0ca450106a6956591aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc8af74e65dbaa0c022ccdd65843b0cd67662cb0055b81e48a54ab54c124c07`

```dockerfile
```

-	Layers:
	-	`sha256:b10d02ee74400fcc336bd4e99e4edd46cb4a0018ef0f18b5c0bfb153f4e18404`  
		Last Modified: Fri, 06 Mar 2026 00:21:45 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:39e05747e040aa04521fe54514ba90522ec2c250c890b2d215b058b53db117b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225635138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45a1a4d83a1ea80478e5286a4368e8e93cf4268519ae923cec47f669b330ae5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Fri, 06 Mar 2026 00:20:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 00:20:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 06 Mar 2026 00:20:48 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 06 Mar 2026 00:20:48 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 00:20:48 GMT
WORKDIR /root
# Fri, 06 Mar 2026 00:20:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43bae8a64ab919bfe317a983a6e223ba905d760574188662362ac17f82fca5a`  
		Last Modified: Fri, 06 Mar 2026 00:21:18 GMT  
		Size: 37.5 MB (37494474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7cd566e4da2372190781a4eb382595d46b7e784c8a1af7de638ab7abb876a`  
		Last Modified: Fri, 06 Mar 2026 00:21:16 GMT  
		Size: 1.3 MB (1273170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baaa18467108c119d6fc8b8b7961886fb61580d0714a0012e16269896cd5859`  
		Last Modified: Fri, 06 Mar 2026 00:21:20 GMT  
		Size: 160.7 MB (160653717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:7eaefd5e6bcf5b5d442af1bca387a5f7f49c127779ac45b18b03da13a7d986b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb50d3451d4bbff18f7af3e34a1eefda1394950c171a9fbc2c3b1b560277d00c`

```dockerfile
```

-	Layers:
	-	`sha256:4dd5f7c6233b8fed4902c20155338f7cc99237052057b642cd8e1cf5e0b46ae4`  
		Last Modified: Fri, 06 Mar 2026 00:21:16 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:1e79efd46afee2b5c12be6200a9547e26fd1e75492b14e2a44fbc549f88f8536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 MB (309723442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72643dbfff39225ae8e46fbafbe481d2c3927ee0bd2a9c57d13614103f3e10f5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Fri, 06 Mar 2026 00:20:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 00:20:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 06 Mar 2026 00:20:56 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 06 Mar 2026 00:20:56 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 00:20:56 GMT
WORKDIR /root
# Fri, 06 Mar 2026 00:21:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68833b8860f3f32f0b393f82d6a208b74aa83d5804a1d9ab4b4ee48a3bd80a7b`  
		Last Modified: Fri, 06 Mar 2026 00:21:40 GMT  
		Size: 42.3 MB (42291717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0a8f75efd4bef95965c7fea5ec957210cfb4f7cfb8ee8870548c2502a88105`  
		Last Modified: Fri, 06 Mar 2026 00:21:38 GMT  
		Size: 1.6 MB (1564523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42318ba95572b11796a1c9d780aa04909d644538cc20ee5cf737262f2c22bfe5`  
		Last Modified: Fri, 06 Mar 2026 00:21:47 GMT  
		Size: 235.7 MB (235727072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:074d7f80b37076d41ea85ae0a0f4563bdf504bc720e6c1aed0344cf9e23415cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2011b4c902d628294980bc2be5d6a24f4186c8db02fa114f2e2ceb69b6fa868`

```dockerfile
```

-	Layers:
	-	`sha256:5373b3825806b03b920125eae61eaa86952ab43330b19a28b767b2c84cfadc28`  
		Last Modified: Fri, 06 Mar 2026 00:21:38 GMT  
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
$ docker pull dart@sha256:7ca43dc0a97bf5420533955af8081a76fd15c4b6f323d30fee9ef0e837c2da73
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
$ docker pull dart@sha256:1c5c80214dcda5103ce6a2d1ebb369ee3c9f3aa8bce99b034a7b87b952799859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311295869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8250ddf92e72abca3288d3f095cd498aa2fead750b20dc02685aa5d3a9926296`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Fri, 06 Mar 2026 00:21:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 00:21:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 06 Mar 2026 00:21:04 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 06 Mar 2026 00:21:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 00:21:04 GMT
WORKDIR /root
# Fri, 06 Mar 2026 00:21:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ae1380938bad3262dfec743c25edb03489a257cce6214a0e8fc279cd31fbef`  
		Last Modified: Fri, 06 Mar 2026 00:21:46 GMT  
		Size: 42.5 MB (42492345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c381b60c3acba3839fa880b174bcccb173f7f01e16d31b07dc2fa8f02ed841`  
		Last Modified: Fri, 06 Mar 2026 00:21:45 GMT  
		Size: 1.9 MB (1870171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9972a34f550f06085aa60628dcb9ab6bc1e01a0e6caff8c6329962ccb952c30`  
		Last Modified: Fri, 06 Mar 2026 00:21:50 GMT  
		Size: 237.2 MB (237154689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:d84eb9dd45596cad707b69f6899bf73438c0f21f3dc2d0ca450106a6956591aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc8af74e65dbaa0c022ccdd65843b0cd67662cb0055b81e48a54ab54c124c07`

```dockerfile
```

-	Layers:
	-	`sha256:b10d02ee74400fcc336bd4e99e4edd46cb4a0018ef0f18b5c0bfb153f4e18404`  
		Last Modified: Fri, 06 Mar 2026 00:21:45 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:39e05747e040aa04521fe54514ba90522ec2c250c890b2d215b058b53db117b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225635138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45a1a4d83a1ea80478e5286a4368e8e93cf4268519ae923cec47f669b330ae5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Fri, 06 Mar 2026 00:20:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 00:20:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 06 Mar 2026 00:20:48 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 06 Mar 2026 00:20:48 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 00:20:48 GMT
WORKDIR /root
# Fri, 06 Mar 2026 00:20:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43bae8a64ab919bfe317a983a6e223ba905d760574188662362ac17f82fca5a`  
		Last Modified: Fri, 06 Mar 2026 00:21:18 GMT  
		Size: 37.5 MB (37494474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7cd566e4da2372190781a4eb382595d46b7e784c8a1af7de638ab7abb876a`  
		Last Modified: Fri, 06 Mar 2026 00:21:16 GMT  
		Size: 1.3 MB (1273170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baaa18467108c119d6fc8b8b7961886fb61580d0714a0012e16269896cd5859`  
		Last Modified: Fri, 06 Mar 2026 00:21:20 GMT  
		Size: 160.7 MB (160653717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7eaefd5e6bcf5b5d442af1bca387a5f7f49c127779ac45b18b03da13a7d986b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb50d3451d4bbff18f7af3e34a1eefda1394950c171a9fbc2c3b1b560277d00c`

```dockerfile
```

-	Layers:
	-	`sha256:4dd5f7c6233b8fed4902c20155338f7cc99237052057b642cd8e1cf5e0b46ae4`  
		Last Modified: Fri, 06 Mar 2026 00:21:16 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:1e79efd46afee2b5c12be6200a9547e26fd1e75492b14e2a44fbc549f88f8536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 MB (309723442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72643dbfff39225ae8e46fbafbe481d2c3927ee0bd2a9c57d13614103f3e10f5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Fri, 06 Mar 2026 00:20:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 00:20:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 06 Mar 2026 00:20:56 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 06 Mar 2026 00:20:56 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 00:20:56 GMT
WORKDIR /root
# Fri, 06 Mar 2026 00:21:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=953b618cdaacbabb22678fb3543510b8d2b5ae124e360a80d85858abe7b11ec6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6b30e245720fbb0585be6941345ca7313036f3969c49596c0f2ca7675aa027bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ce194b74edcdef1db97682cace739a74b0a1c83b1ea5ac270beb6e1463d21dd;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8de5cca0da4a2d8f3358d37c7adabba06c7b1d82f124ed747d2bb6f7b5fc884f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-210.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68833b8860f3f32f0b393f82d6a208b74aa83d5804a1d9ab4b4ee48a3bd80a7b`  
		Last Modified: Fri, 06 Mar 2026 00:21:40 GMT  
		Size: 42.3 MB (42291717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0a8f75efd4bef95965c7fea5ec957210cfb4f7cfb8ee8870548c2502a88105`  
		Last Modified: Fri, 06 Mar 2026 00:21:38 GMT  
		Size: 1.6 MB (1564523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42318ba95572b11796a1c9d780aa04909d644538cc20ee5cf737262f2c22bfe5`  
		Last Modified: Fri, 06 Mar 2026 00:21:47 GMT  
		Size: 235.7 MB (235727072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:074d7f80b37076d41ea85ae0a0f4563bdf504bc720e6c1aed0344cf9e23415cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2011b4c902d628294980bc2be5d6a24f4186c8db02fa114f2e2ceb69b6fa868`

```dockerfile
```

-	Layers:
	-	`sha256:5373b3825806b03b920125eae61eaa86952ab43330b19a28b767b2c84cfadc28`  
		Last Modified: Fri, 06 Mar 2026 00:21:38 GMT  
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
$ docker pull dart@sha256:4fa392688a1d8d122df58e791bb26c512732b9da69a3cb93686f18359768007a
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
$ docker pull dart@sha256:fdbce01fa8eec7bb2822267e0ed775d08ce93d3c1e60282e8c253962424ab4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307072943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f879955ebe22e08effaed6fb6a8f41a81457fc17f028cc451a727eff5341cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 17:27:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 17:27:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 17:27:22 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 17:27:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 17:27:22 GMT
WORKDIR /root
# Tue, 10 Mar 2026 17:27:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebaecf214b547a6eda20ae95caf4304a5e54511b745bd713465e48929ce00b9`  
		Last Modified: Tue, 10 Mar 2026 17:28:02 GMT  
		Size: 42.5 MB (42492259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbd30f011011b8c2b7951eec0bcd9e2b825ea1861dd5a084202b4c38a2c452f`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 1.9 MB (1870165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c87d3eb32792c781e11ede467bc263de71e2bd74dadba1e51c3376c0d17a916`  
		Last Modified: Tue, 10 Mar 2026 17:28:05 GMT  
		Size: 232.9 MB (232931855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:58581453812e031801ddfc96c8345de01611cfdf2941c8592691c75f817d91a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2335bd3715c8c0d4279fa706a4758531977406a2939f71265494982df7333b`

```dockerfile
```

-	Layers:
	-	`sha256:8f8329fe3cc90fe89b9b69af2f805e93f818fd0a0e86b86968b5b24e2e436c32`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:a45bbff844d3b258518f851b89a07be1eda97e2181357ebe21e2690452a71541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222903412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88971476d67c33dce48662e0f31c2c2d0b26528593accb753f9718922430c82`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 18:01:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 18:01:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 18:01:07 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 18:01:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 18:01:07 GMT
WORKDIR /root
# Tue, 10 Mar 2026 18:01:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1939b75bceac29b04b5c1bb3785f4216aa28ce925e1d4a2e58a709ab8bcd23c2`  
		Last Modified: Tue, 10 Mar 2026 18:01:38 GMT  
		Size: 37.5 MB (37494608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd00857f051f4ba385f8094859364b70743cefeb9f20e140644ec0f587e3c7c`  
		Last Modified: Tue, 10 Mar 2026 18:01:36 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95990048096302ee3ecf1ba4cbed0ee0d5b8f61fef1fa1c5806b1438a88a2467`  
		Last Modified: Tue, 10 Mar 2026 18:01:40 GMT  
		Size: 157.9 MB (157921874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:1f93484d6ebc0c4a4ec84e0141f7de6d63bd7b4eaa8c593b0c69fac8c9794c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2dd2a1d7f7bcc145efccdab1dc09540c0e44ad4bfb01d9ad15fb428ce01de41`

```dockerfile
```

-	Layers:
	-	`sha256:71f143846e3cb7bb8a517a810fd9e77b3e2e98571190593b9f7493ef4242d0f5`  
		Last Modified: Tue, 10 Mar 2026 18:01:36 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0a9028f3593f5f6ec72eed477d158bcc4af54ccfe84792097894c3c0ca130bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305432011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9316303ea5cedd9dea99cfa15b11f310b646e6dd73ca9955a8252b21bd1936`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 17:27:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 17:27:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 17:27:21 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 17:27:21 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 17:27:21 GMT
WORKDIR /root
# Tue, 10 Mar 2026 17:27:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a3338f6e2aecfc8130b13ef69938e83589c18b2dca07ceab488685b5d6d14e`  
		Last Modified: Tue, 10 Mar 2026 17:28:02 GMT  
		Size: 42.3 MB (42291774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7229b6a4dd4f0a0478c7caf635e78856040c6f0500e1272bab9ccb7a425466b8`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 1.6 MB (1564520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b565de8325d2f94cca17e82b49f893ce4e9101988c327a10a6c488dadfbb8a2a`  
		Last Modified: Tue, 10 Mar 2026 17:28:06 GMT  
		Size: 231.4 MB (231435587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:eab5fc1888558d46ea75a039426ec9da378b199f20f430e2ca8d1422b635b20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4be896671db4ed16ec0ac70ab95f211f84eb86e3603740446ea12244a63ea`

```dockerfile
```

-	Layers:
	-	`sha256:b068bffec839c81d72f042e72cb74ec732a4b79e335eb2ec0e1194e6d493391e`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; riscv64

```console
$ docker pull dart@sha256:3c50bd3f77c48dabf0745da10733e901a29f50f48375204ffce8b1f8cb3d26b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bbe8353f4bf2c2b74bbfc9d6cd971f71c61c6e854327256bd0e0dfeeb70fb2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:47:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 26 Feb 2026 21:47:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 21:47:17 GMT
WORKDIR /root
# Thu, 26 Feb 2026 21:48:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005b5410669f900e219d8f1011496036e8e069aa48a198a6760555d1e565862`  
		Last Modified: Thu, 26 Feb 2026 21:52:24 GMT  
		Size: 41.6 MB (41560724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b398538cbb3cf53074f900bb3c39189de10e24ab8ad79bc08944898c0008d0`  
		Last Modified: Thu, 26 Feb 2026 21:52:08 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb387d36d548d74ab36773195694e1529dca0153f6b401118c2fad500d6a3be`  
		Last Modified: Thu, 26 Feb 2026 21:52:43 GMT  
		Size: 180.5 MB (180483956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:b2100c2dbdb91555037b5c28a91c8690920255dd893f5c37769d0ed072fce4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2de089cc2eb0543729a77991a9982b076142756be16a0561e5b7d667a651270`

```dockerfile
```

-	Layers:
	-	`sha256:36a836d347e4af15c77b9ab5afc85d735357d7d81cfc4fd67d121798ac3a6a2c`  
		Last Modified: Thu, 26 Feb 2026 21:52:05 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:4fa392688a1d8d122df58e791bb26c512732b9da69a3cb93686f18359768007a
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
$ docker pull dart@sha256:fdbce01fa8eec7bb2822267e0ed775d08ce93d3c1e60282e8c253962424ab4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307072943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f879955ebe22e08effaed6fb6a8f41a81457fc17f028cc451a727eff5341cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 17:27:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 17:27:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 17:27:22 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 17:27:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 17:27:22 GMT
WORKDIR /root
# Tue, 10 Mar 2026 17:27:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebaecf214b547a6eda20ae95caf4304a5e54511b745bd713465e48929ce00b9`  
		Last Modified: Tue, 10 Mar 2026 17:28:02 GMT  
		Size: 42.5 MB (42492259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbd30f011011b8c2b7951eec0bcd9e2b825ea1861dd5a084202b4c38a2c452f`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 1.9 MB (1870165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c87d3eb32792c781e11ede467bc263de71e2bd74dadba1e51c3376c0d17a916`  
		Last Modified: Tue, 10 Mar 2026 17:28:05 GMT  
		Size: 232.9 MB (232931855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:58581453812e031801ddfc96c8345de01611cfdf2941c8592691c75f817d91a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2335bd3715c8c0d4279fa706a4758531977406a2939f71265494982df7333b`

```dockerfile
```

-	Layers:
	-	`sha256:8f8329fe3cc90fe89b9b69af2f805e93f818fd0a0e86b86968b5b24e2e436c32`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:a45bbff844d3b258518f851b89a07be1eda97e2181357ebe21e2690452a71541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222903412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88971476d67c33dce48662e0f31c2c2d0b26528593accb753f9718922430c82`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 18:01:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 18:01:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 18:01:07 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 18:01:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 18:01:07 GMT
WORKDIR /root
# Tue, 10 Mar 2026 18:01:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1939b75bceac29b04b5c1bb3785f4216aa28ce925e1d4a2e58a709ab8bcd23c2`  
		Last Modified: Tue, 10 Mar 2026 18:01:38 GMT  
		Size: 37.5 MB (37494608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd00857f051f4ba385f8094859364b70743cefeb9f20e140644ec0f587e3c7c`  
		Last Modified: Tue, 10 Mar 2026 18:01:36 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95990048096302ee3ecf1ba4cbed0ee0d5b8f61fef1fa1c5806b1438a88a2467`  
		Last Modified: Tue, 10 Mar 2026 18:01:40 GMT  
		Size: 157.9 MB (157921874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1f93484d6ebc0c4a4ec84e0141f7de6d63bd7b4eaa8c593b0c69fac8c9794c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2dd2a1d7f7bcc145efccdab1dc09540c0e44ad4bfb01d9ad15fb428ce01de41`

```dockerfile
```

-	Layers:
	-	`sha256:71f143846e3cb7bb8a517a810fd9e77b3e2e98571190593b9f7493ef4242d0f5`  
		Last Modified: Tue, 10 Mar 2026 18:01:36 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0a9028f3593f5f6ec72eed477d158bcc4af54ccfe84792097894c3c0ca130bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305432011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9316303ea5cedd9dea99cfa15b11f310b646e6dd73ca9955a8252b21bd1936`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 17:27:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 17:27:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 17:27:21 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 17:27:21 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 17:27:21 GMT
WORKDIR /root
# Tue, 10 Mar 2026 17:27:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a3338f6e2aecfc8130b13ef69938e83589c18b2dca07ceab488685b5d6d14e`  
		Last Modified: Tue, 10 Mar 2026 17:28:02 GMT  
		Size: 42.3 MB (42291774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7229b6a4dd4f0a0478c7caf635e78856040c6f0500e1272bab9ccb7a425466b8`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 1.6 MB (1564520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b565de8325d2f94cca17e82b49f893ce4e9101988c327a10a6c488dadfbb8a2a`  
		Last Modified: Tue, 10 Mar 2026 17:28:06 GMT  
		Size: 231.4 MB (231435587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:eab5fc1888558d46ea75a039426ec9da378b199f20f430e2ca8d1422b635b20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4be896671db4ed16ec0ac70ab95f211f84eb86e3603740446ea12244a63ea`

```dockerfile
```

-	Layers:
	-	`sha256:b068bffec839c81d72f042e72cb74ec732a4b79e335eb2ec0e1194e6d493391e`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; riscv64

```console
$ docker pull dart@sha256:3c50bd3f77c48dabf0745da10733e901a29f50f48375204ffce8b1f8cb3d26b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bbe8353f4bf2c2b74bbfc9d6cd971f71c61c6e854327256bd0e0dfeeb70fb2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:47:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 26 Feb 2026 21:47:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 21:47:17 GMT
WORKDIR /root
# Thu, 26 Feb 2026 21:48:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005b5410669f900e219d8f1011496036e8e069aa48a198a6760555d1e565862`  
		Last Modified: Thu, 26 Feb 2026 21:52:24 GMT  
		Size: 41.6 MB (41560724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b398538cbb3cf53074f900bb3c39189de10e24ab8ad79bc08944898c0008d0`  
		Last Modified: Thu, 26 Feb 2026 21:52:08 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb387d36d548d74ab36773195694e1529dca0153f6b401118c2fad500d6a3be`  
		Last Modified: Thu, 26 Feb 2026 21:52:43 GMT  
		Size: 180.5 MB (180483956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b2100c2dbdb91555037b5c28a91c8690920255dd893f5c37769d0ed072fce4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2de089cc2eb0543729a77991a9982b076142756be16a0561e5b7d667a651270`

```dockerfile
```

-	Layers:
	-	`sha256:36a836d347e4af15c77b9ab5afc85d735357d7d81cfc4fd67d121798ac3a6a2c`  
		Last Modified: Thu, 26 Feb 2026 21:52:05 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:4fa392688a1d8d122df58e791bb26c512732b9da69a3cb93686f18359768007a
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
$ docker pull dart@sha256:fdbce01fa8eec7bb2822267e0ed775d08ce93d3c1e60282e8c253962424ab4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307072943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f879955ebe22e08effaed6fb6a8f41a81457fc17f028cc451a727eff5341cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 17:27:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 17:27:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 17:27:22 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 17:27:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 17:27:22 GMT
WORKDIR /root
# Tue, 10 Mar 2026 17:27:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebaecf214b547a6eda20ae95caf4304a5e54511b745bd713465e48929ce00b9`  
		Last Modified: Tue, 10 Mar 2026 17:28:02 GMT  
		Size: 42.5 MB (42492259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbd30f011011b8c2b7951eec0bcd9e2b825ea1861dd5a084202b4c38a2c452f`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 1.9 MB (1870165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c87d3eb32792c781e11ede467bc263de71e2bd74dadba1e51c3376c0d17a916`  
		Last Modified: Tue, 10 Mar 2026 17:28:05 GMT  
		Size: 232.9 MB (232931855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:58581453812e031801ddfc96c8345de01611cfdf2941c8592691c75f817d91a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2335bd3715c8c0d4279fa706a4758531977406a2939f71265494982df7333b`

```dockerfile
```

-	Layers:
	-	`sha256:8f8329fe3cc90fe89b9b69af2f805e93f818fd0a0e86b86968b5b24e2e436c32`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:a45bbff844d3b258518f851b89a07be1eda97e2181357ebe21e2690452a71541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222903412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88971476d67c33dce48662e0f31c2c2d0b26528593accb753f9718922430c82`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 18:01:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 18:01:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 18:01:07 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 18:01:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 18:01:07 GMT
WORKDIR /root
# Tue, 10 Mar 2026 18:01:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1939b75bceac29b04b5c1bb3785f4216aa28ce925e1d4a2e58a709ab8bcd23c2`  
		Last Modified: Tue, 10 Mar 2026 18:01:38 GMT  
		Size: 37.5 MB (37494608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd00857f051f4ba385f8094859364b70743cefeb9f20e140644ec0f587e3c7c`  
		Last Modified: Tue, 10 Mar 2026 18:01:36 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95990048096302ee3ecf1ba4cbed0ee0d5b8f61fef1fa1c5806b1438a88a2467`  
		Last Modified: Tue, 10 Mar 2026 18:01:40 GMT  
		Size: 157.9 MB (157921874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:1f93484d6ebc0c4a4ec84e0141f7de6d63bd7b4eaa8c593b0c69fac8c9794c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2dd2a1d7f7bcc145efccdab1dc09540c0e44ad4bfb01d9ad15fb428ce01de41`

```dockerfile
```

-	Layers:
	-	`sha256:71f143846e3cb7bb8a517a810fd9e77b3e2e98571190593b9f7493ef4242d0f5`  
		Last Modified: Tue, 10 Mar 2026 18:01:36 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0a9028f3593f5f6ec72eed477d158bcc4af54ccfe84792097894c3c0ca130bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305432011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9316303ea5cedd9dea99cfa15b11f310b646e6dd73ca9955a8252b21bd1936`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 17:27:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 17:27:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 17:27:21 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 17:27:21 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 17:27:21 GMT
WORKDIR /root
# Tue, 10 Mar 2026 17:27:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a3338f6e2aecfc8130b13ef69938e83589c18b2dca07ceab488685b5d6d14e`  
		Last Modified: Tue, 10 Mar 2026 17:28:02 GMT  
		Size: 42.3 MB (42291774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7229b6a4dd4f0a0478c7caf635e78856040c6f0500e1272bab9ccb7a425466b8`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 1.6 MB (1564520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b565de8325d2f94cca17e82b49f893ce4e9101988c327a10a6c488dadfbb8a2a`  
		Last Modified: Tue, 10 Mar 2026 17:28:06 GMT  
		Size: 231.4 MB (231435587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:eab5fc1888558d46ea75a039426ec9da378b199f20f430e2ca8d1422b635b20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4be896671db4ed16ec0ac70ab95f211f84eb86e3603740446ea12244a63ea`

```dockerfile
```

-	Layers:
	-	`sha256:b068bffec839c81d72f042e72cb74ec732a4b79e335eb2ec0e1194e6d493391e`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; riscv64

```console
$ docker pull dart@sha256:3c50bd3f77c48dabf0745da10733e901a29f50f48375204ffce8b1f8cb3d26b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bbe8353f4bf2c2b74bbfc9d6cd971f71c61c6e854327256bd0e0dfeeb70fb2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:47:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 26 Feb 2026 21:47:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 21:47:17 GMT
WORKDIR /root
# Thu, 26 Feb 2026 21:48:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005b5410669f900e219d8f1011496036e8e069aa48a198a6760555d1e565862`  
		Last Modified: Thu, 26 Feb 2026 21:52:24 GMT  
		Size: 41.6 MB (41560724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b398538cbb3cf53074f900bb3c39189de10e24ab8ad79bc08944898c0008d0`  
		Last Modified: Thu, 26 Feb 2026 21:52:08 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb387d36d548d74ab36773195694e1529dca0153f6b401118c2fad500d6a3be`  
		Last Modified: Thu, 26 Feb 2026 21:52:43 GMT  
		Size: 180.5 MB (180483956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:b2100c2dbdb91555037b5c28a91c8690920255dd893f5c37769d0ed072fce4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2de089cc2eb0543729a77991a9982b076142756be16a0561e5b7d667a651270`

```dockerfile
```

-	Layers:
	-	`sha256:36a836d347e4af15c77b9ab5afc85d735357d7d81cfc4fd67d121798ac3a6a2c`  
		Last Modified: Thu, 26 Feb 2026 21:52:05 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:4fa392688a1d8d122df58e791bb26c512732b9da69a3cb93686f18359768007a
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
$ docker pull dart@sha256:fdbce01fa8eec7bb2822267e0ed775d08ce93d3c1e60282e8c253962424ab4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307072943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f879955ebe22e08effaed6fb6a8f41a81457fc17f028cc451a727eff5341cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 17:27:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 17:27:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 17:27:22 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 17:27:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 17:27:22 GMT
WORKDIR /root
# Tue, 10 Mar 2026 17:27:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebaecf214b547a6eda20ae95caf4304a5e54511b745bd713465e48929ce00b9`  
		Last Modified: Tue, 10 Mar 2026 17:28:02 GMT  
		Size: 42.5 MB (42492259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbd30f011011b8c2b7951eec0bcd9e2b825ea1861dd5a084202b4c38a2c452f`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 1.9 MB (1870165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c87d3eb32792c781e11ede467bc263de71e2bd74dadba1e51c3376c0d17a916`  
		Last Modified: Tue, 10 Mar 2026 17:28:05 GMT  
		Size: 232.9 MB (232931855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:58581453812e031801ddfc96c8345de01611cfdf2941c8592691c75f817d91a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2335bd3715c8c0d4279fa706a4758531977406a2939f71265494982df7333b`

```dockerfile
```

-	Layers:
	-	`sha256:8f8329fe3cc90fe89b9b69af2f805e93f818fd0a0e86b86968b5b24e2e436c32`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:a45bbff844d3b258518f851b89a07be1eda97e2181357ebe21e2690452a71541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222903412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88971476d67c33dce48662e0f31c2c2d0b26528593accb753f9718922430c82`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 18:01:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 18:01:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 18:01:07 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 18:01:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 18:01:07 GMT
WORKDIR /root
# Tue, 10 Mar 2026 18:01:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1939b75bceac29b04b5c1bb3785f4216aa28ce925e1d4a2e58a709ab8bcd23c2`  
		Last Modified: Tue, 10 Mar 2026 18:01:38 GMT  
		Size: 37.5 MB (37494608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd00857f051f4ba385f8094859364b70743cefeb9f20e140644ec0f587e3c7c`  
		Last Modified: Tue, 10 Mar 2026 18:01:36 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95990048096302ee3ecf1ba4cbed0ee0d5b8f61fef1fa1c5806b1438a88a2467`  
		Last Modified: Tue, 10 Mar 2026 18:01:40 GMT  
		Size: 157.9 MB (157921874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1f93484d6ebc0c4a4ec84e0141f7de6d63bd7b4eaa8c593b0c69fac8c9794c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2dd2a1d7f7bcc145efccdab1dc09540c0e44ad4bfb01d9ad15fb428ce01de41`

```dockerfile
```

-	Layers:
	-	`sha256:71f143846e3cb7bb8a517a810fd9e77b3e2e98571190593b9f7493ef4242d0f5`  
		Last Modified: Tue, 10 Mar 2026 18:01:36 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0a9028f3593f5f6ec72eed477d158bcc4af54ccfe84792097894c3c0ca130bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305432011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9316303ea5cedd9dea99cfa15b11f310b646e6dd73ca9955a8252b21bd1936`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 17:27:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 17:27:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 10 Mar 2026 17:27:21 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 10 Mar 2026 17:27:21 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 17:27:21 GMT
WORKDIR /root
# Tue, 10 Mar 2026 17:27:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e646de59cf9bfdba8ecdca7b27a7d6bda3bd14b4a2256728b58172fb44bbd672;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1a92197956e98fb98f2a10a841337ca3e21ab072401fadbe513a4009c0c81d7f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c594d646319a755d332e8d438e1a0693214e73b2fbb798d0a72d909373ba6646;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=132f9f10a374c67ba385b53aabf9add9a026fe3a4b3f19a50a1548c53a1f5f3a;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a3338f6e2aecfc8130b13ef69938e83589c18b2dca07ceab488685b5d6d14e`  
		Last Modified: Tue, 10 Mar 2026 17:28:02 GMT  
		Size: 42.3 MB (42291774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7229b6a4dd4f0a0478c7caf635e78856040c6f0500e1272bab9ccb7a425466b8`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 1.6 MB (1564520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b565de8325d2f94cca17e82b49f893ce4e9101988c327a10a6c488dadfbb8a2a`  
		Last Modified: Tue, 10 Mar 2026 17:28:06 GMT  
		Size: 231.4 MB (231435587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:eab5fc1888558d46ea75a039426ec9da378b199f20f430e2ca8d1422b635b20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4be896671db4ed16ec0ac70ab95f211f84eb86e3603740446ea12244a63ea`

```dockerfile
```

-	Layers:
	-	`sha256:b068bffec839c81d72f042e72cb74ec732a4b79e335eb2ec0e1194e6d493391e`  
		Last Modified: Tue, 10 Mar 2026 17:28:00 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:3c50bd3f77c48dabf0745da10733e901a29f50f48375204ffce8b1f8cb3d26b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bbe8353f4bf2c2b74bbfc9d6cd971f71c61c6e854327256bd0e0dfeeb70fb2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:47:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 26 Feb 2026 21:47:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 21:47:17 GMT
WORKDIR /root
# Thu, 26 Feb 2026 21:48:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005b5410669f900e219d8f1011496036e8e069aa48a198a6760555d1e565862`  
		Last Modified: Thu, 26 Feb 2026 21:52:24 GMT  
		Size: 41.6 MB (41560724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b398538cbb3cf53074f900bb3c39189de10e24ab8ad79bc08944898c0008d0`  
		Last Modified: Thu, 26 Feb 2026 21:52:08 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb387d36d548d74ab36773195694e1529dca0153f6b401118c2fad500d6a3be`  
		Last Modified: Thu, 26 Feb 2026 21:52:43 GMT  
		Size: 180.5 MB (180483956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b2100c2dbdb91555037b5c28a91c8690920255dd893f5c37769d0ed072fce4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2de089cc2eb0543729a77991a9982b076142756be16a0561e5b7d667a651270`

```dockerfile
```

-	Layers:
	-	`sha256:36a836d347e4af15c77b9ab5afc85d735357d7d81cfc4fd67d121798ac3a6a2c`  
		Last Modified: Thu, 26 Feb 2026 21:52:05 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json
