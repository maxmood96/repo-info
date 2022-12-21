<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:2`](#dart2)
-	[`dart:2-sdk`](#dart2-sdk)
-	[`dart:2.18`](#dart218)
-	[`dart:2.18-sdk`](#dart218-sdk)
-	[`dart:2.18.6`](#dart2186)
-	[`dart:2.18.6-sdk`](#dart2186-sdk)
-	[`dart:2.19.0-444.2.beta`](#dart2190-4442beta)
-	[`dart:2.19.0-444.2.beta-sdk`](#dart2190-4442beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:2`

```console
$ docker pull dart@sha256:d0704c148be11dcfaf2221128ea1f200f19a5acce90396d73b4596b3fa318584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2` - linux; amd64

```console
$ docker pull dart@sha256:f01f9640b241c8bcc9a9cafd7f9e907616e4417523ee956bbfcf938bb769e641
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271928321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f053d1795af04f470caba08091334ee9d6920c0baa93a66cfb26f732f01a770f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:15:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:15:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 02:15:49 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 02:15:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 02:15:49 GMT
WORKDIR /root
# Wed, 21 Dec 2022 02:16:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f93052e58e62ed85a7a429c69eefab2de9abcb0ea08cddf775756a369397cc4`  
		Last Modified: Wed, 21 Dec 2022 02:16:55 GMT  
		Size: 45.1 MB (45073057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a4a8d101c8f583489acf734e17554e63b1f2e68c38e36cce0ed2a1d38a5c76`  
		Last Modified: Wed, 21 Dec 2022 02:16:48 GMT  
		Size: 2.2 MB (2162025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cc094cc3bcdec2368b60911e81ea1a79086d5e291fca585ea0b324cd46ae82`  
		Last Modified: Wed, 21 Dec 2022 02:17:16 GMT  
		Size: 193.3 MB (193296296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2` - linux; arm variant v7

```console
$ docker pull dart@sha256:2d360ee94083fb7a951c62a1983441bfb982a97e2e244cca61da6ec07cafdba8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180607509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7221d08b7e6217647bb8d51885062dd68aac7b60e6e0ed7a2c6ee9a68d19c228`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:00:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad75836ddeea1d435c6db7f3d2e2c8ba7ba9ff6ae8b495bb9d98be60e4fb93`  
		Last Modified: Sat, 17 Dec 2022 03:02:41 GMT  
		Size: 111.8 MB (111786221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:de509b6121dd3e5baa103d54cbb045b10d52da8356cd558d331b0f7c3d1c1820
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.5 MB (189542274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3573f824c49528f0db0955ef95287f5bb709564e08249e5c3d5b982fb9ff208`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:13:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:13:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 13:13:56 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 13:13:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 13:13:56 GMT
WORKDIR /root
# Wed, 21 Dec 2022 13:14:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdff8a458215716fab99b63df7cae1c0e12c9e84020634c3b6afd9512d7181f`  
		Last Modified: Wed, 21 Dec 2022 13:14:48 GMT  
		Size: 45.0 MB (44994592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5ddd0e7b8eeb5bc439dbae37cb86546355e99664fd68fe4239c8b9b11ec51b`  
		Last Modified: Wed, 21 Dec 2022 13:14:43 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830ef74f6bb15b98bebdb90fb766497e905d8fd61c68ffa5f88cf8971403c548`  
		Last Modified: Wed, 21 Dec 2022 13:14:56 GMT  
		Size: 112.9 MB (112940727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2-sdk`

```console
$ docker pull dart@sha256:d0704c148be11dcfaf2221128ea1f200f19a5acce90396d73b4596b3fa318584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2-sdk` - linux; amd64

```console
$ docker pull dart@sha256:f01f9640b241c8bcc9a9cafd7f9e907616e4417523ee956bbfcf938bb769e641
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271928321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f053d1795af04f470caba08091334ee9d6920c0baa93a66cfb26f732f01a770f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:15:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:15:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 02:15:49 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 02:15:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 02:15:49 GMT
WORKDIR /root
# Wed, 21 Dec 2022 02:16:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f93052e58e62ed85a7a429c69eefab2de9abcb0ea08cddf775756a369397cc4`  
		Last Modified: Wed, 21 Dec 2022 02:16:55 GMT  
		Size: 45.1 MB (45073057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a4a8d101c8f583489acf734e17554e63b1f2e68c38e36cce0ed2a1d38a5c76`  
		Last Modified: Wed, 21 Dec 2022 02:16:48 GMT  
		Size: 2.2 MB (2162025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cc094cc3bcdec2368b60911e81ea1a79086d5e291fca585ea0b324cd46ae82`  
		Last Modified: Wed, 21 Dec 2022 02:17:16 GMT  
		Size: 193.3 MB (193296296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2d360ee94083fb7a951c62a1983441bfb982a97e2e244cca61da6ec07cafdba8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180607509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7221d08b7e6217647bb8d51885062dd68aac7b60e6e0ed7a2c6ee9a68d19c228`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:00:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad75836ddeea1d435c6db7f3d2e2c8ba7ba9ff6ae8b495bb9d98be60e4fb93`  
		Last Modified: Sat, 17 Dec 2022 03:02:41 GMT  
		Size: 111.8 MB (111786221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:de509b6121dd3e5baa103d54cbb045b10d52da8356cd558d331b0f7c3d1c1820
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.5 MB (189542274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3573f824c49528f0db0955ef95287f5bb709564e08249e5c3d5b982fb9ff208`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:13:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:13:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 13:13:56 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 13:13:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 13:13:56 GMT
WORKDIR /root
# Wed, 21 Dec 2022 13:14:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdff8a458215716fab99b63df7cae1c0e12c9e84020634c3b6afd9512d7181f`  
		Last Modified: Wed, 21 Dec 2022 13:14:48 GMT  
		Size: 45.0 MB (44994592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5ddd0e7b8eeb5bc439dbae37cb86546355e99664fd68fe4239c8b9b11ec51b`  
		Last Modified: Wed, 21 Dec 2022 13:14:43 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830ef74f6bb15b98bebdb90fb766497e905d8fd61c68ffa5f88cf8971403c548`  
		Last Modified: Wed, 21 Dec 2022 13:14:56 GMT  
		Size: 112.9 MB (112940727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.18`

```console
$ docker pull dart@sha256:d0704c148be11dcfaf2221128ea1f200f19a5acce90396d73b4596b3fa318584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.18` - linux; amd64

```console
$ docker pull dart@sha256:f01f9640b241c8bcc9a9cafd7f9e907616e4417523ee956bbfcf938bb769e641
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271928321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f053d1795af04f470caba08091334ee9d6920c0baa93a66cfb26f732f01a770f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:15:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:15:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 02:15:49 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 02:15:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 02:15:49 GMT
WORKDIR /root
# Wed, 21 Dec 2022 02:16:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f93052e58e62ed85a7a429c69eefab2de9abcb0ea08cddf775756a369397cc4`  
		Last Modified: Wed, 21 Dec 2022 02:16:55 GMT  
		Size: 45.1 MB (45073057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a4a8d101c8f583489acf734e17554e63b1f2e68c38e36cce0ed2a1d38a5c76`  
		Last Modified: Wed, 21 Dec 2022 02:16:48 GMT  
		Size: 2.2 MB (2162025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cc094cc3bcdec2368b60911e81ea1a79086d5e291fca585ea0b324cd46ae82`  
		Last Modified: Wed, 21 Dec 2022 02:17:16 GMT  
		Size: 193.3 MB (193296296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.18` - linux; arm variant v7

```console
$ docker pull dart@sha256:2d360ee94083fb7a951c62a1983441bfb982a97e2e244cca61da6ec07cafdba8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180607509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7221d08b7e6217647bb8d51885062dd68aac7b60e6e0ed7a2c6ee9a68d19c228`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:00:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad75836ddeea1d435c6db7f3d2e2c8ba7ba9ff6ae8b495bb9d98be60e4fb93`  
		Last Modified: Sat, 17 Dec 2022 03:02:41 GMT  
		Size: 111.8 MB (111786221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.18` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:de509b6121dd3e5baa103d54cbb045b10d52da8356cd558d331b0f7c3d1c1820
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.5 MB (189542274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3573f824c49528f0db0955ef95287f5bb709564e08249e5c3d5b982fb9ff208`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:13:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:13:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 13:13:56 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 13:13:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 13:13:56 GMT
WORKDIR /root
# Wed, 21 Dec 2022 13:14:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdff8a458215716fab99b63df7cae1c0e12c9e84020634c3b6afd9512d7181f`  
		Last Modified: Wed, 21 Dec 2022 13:14:48 GMT  
		Size: 45.0 MB (44994592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5ddd0e7b8eeb5bc439dbae37cb86546355e99664fd68fe4239c8b9b11ec51b`  
		Last Modified: Wed, 21 Dec 2022 13:14:43 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830ef74f6bb15b98bebdb90fb766497e905d8fd61c68ffa5f88cf8971403c548`  
		Last Modified: Wed, 21 Dec 2022 13:14:56 GMT  
		Size: 112.9 MB (112940727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.18-sdk`

```console
$ docker pull dart@sha256:d0704c148be11dcfaf2221128ea1f200f19a5acce90396d73b4596b3fa318584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.18-sdk` - linux; amd64

```console
$ docker pull dart@sha256:f01f9640b241c8bcc9a9cafd7f9e907616e4417523ee956bbfcf938bb769e641
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271928321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f053d1795af04f470caba08091334ee9d6920c0baa93a66cfb26f732f01a770f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:15:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:15:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 02:15:49 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 02:15:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 02:15:49 GMT
WORKDIR /root
# Wed, 21 Dec 2022 02:16:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f93052e58e62ed85a7a429c69eefab2de9abcb0ea08cddf775756a369397cc4`  
		Last Modified: Wed, 21 Dec 2022 02:16:55 GMT  
		Size: 45.1 MB (45073057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a4a8d101c8f583489acf734e17554e63b1f2e68c38e36cce0ed2a1d38a5c76`  
		Last Modified: Wed, 21 Dec 2022 02:16:48 GMT  
		Size: 2.2 MB (2162025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cc094cc3bcdec2368b60911e81ea1a79086d5e291fca585ea0b324cd46ae82`  
		Last Modified: Wed, 21 Dec 2022 02:17:16 GMT  
		Size: 193.3 MB (193296296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.18-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2d360ee94083fb7a951c62a1983441bfb982a97e2e244cca61da6ec07cafdba8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180607509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7221d08b7e6217647bb8d51885062dd68aac7b60e6e0ed7a2c6ee9a68d19c228`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:00:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad75836ddeea1d435c6db7f3d2e2c8ba7ba9ff6ae8b495bb9d98be60e4fb93`  
		Last Modified: Sat, 17 Dec 2022 03:02:41 GMT  
		Size: 111.8 MB (111786221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.18-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:de509b6121dd3e5baa103d54cbb045b10d52da8356cd558d331b0f7c3d1c1820
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.5 MB (189542274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3573f824c49528f0db0955ef95287f5bb709564e08249e5c3d5b982fb9ff208`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:13:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:13:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 13:13:56 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 13:13:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 13:13:56 GMT
WORKDIR /root
# Wed, 21 Dec 2022 13:14:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdff8a458215716fab99b63df7cae1c0e12c9e84020634c3b6afd9512d7181f`  
		Last Modified: Wed, 21 Dec 2022 13:14:48 GMT  
		Size: 45.0 MB (44994592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5ddd0e7b8eeb5bc439dbae37cb86546355e99664fd68fe4239c8b9b11ec51b`  
		Last Modified: Wed, 21 Dec 2022 13:14:43 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830ef74f6bb15b98bebdb90fb766497e905d8fd61c68ffa5f88cf8971403c548`  
		Last Modified: Wed, 21 Dec 2022 13:14:56 GMT  
		Size: 112.9 MB (112940727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.18.6`

```console
$ docker pull dart@sha256:d0704c148be11dcfaf2221128ea1f200f19a5acce90396d73b4596b3fa318584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.18.6` - linux; amd64

```console
$ docker pull dart@sha256:f01f9640b241c8bcc9a9cafd7f9e907616e4417523ee956bbfcf938bb769e641
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271928321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f053d1795af04f470caba08091334ee9d6920c0baa93a66cfb26f732f01a770f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:15:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:15:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 02:15:49 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 02:15:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 02:15:49 GMT
WORKDIR /root
# Wed, 21 Dec 2022 02:16:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f93052e58e62ed85a7a429c69eefab2de9abcb0ea08cddf775756a369397cc4`  
		Last Modified: Wed, 21 Dec 2022 02:16:55 GMT  
		Size: 45.1 MB (45073057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a4a8d101c8f583489acf734e17554e63b1f2e68c38e36cce0ed2a1d38a5c76`  
		Last Modified: Wed, 21 Dec 2022 02:16:48 GMT  
		Size: 2.2 MB (2162025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cc094cc3bcdec2368b60911e81ea1a79086d5e291fca585ea0b324cd46ae82`  
		Last Modified: Wed, 21 Dec 2022 02:17:16 GMT  
		Size: 193.3 MB (193296296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.18.6` - linux; arm variant v7

```console
$ docker pull dart@sha256:2d360ee94083fb7a951c62a1983441bfb982a97e2e244cca61da6ec07cafdba8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180607509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7221d08b7e6217647bb8d51885062dd68aac7b60e6e0ed7a2c6ee9a68d19c228`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:00:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad75836ddeea1d435c6db7f3d2e2c8ba7ba9ff6ae8b495bb9d98be60e4fb93`  
		Last Modified: Sat, 17 Dec 2022 03:02:41 GMT  
		Size: 111.8 MB (111786221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.18.6` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:de509b6121dd3e5baa103d54cbb045b10d52da8356cd558d331b0f7c3d1c1820
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.5 MB (189542274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3573f824c49528f0db0955ef95287f5bb709564e08249e5c3d5b982fb9ff208`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:13:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:13:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 13:13:56 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 13:13:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 13:13:56 GMT
WORKDIR /root
# Wed, 21 Dec 2022 13:14:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdff8a458215716fab99b63df7cae1c0e12c9e84020634c3b6afd9512d7181f`  
		Last Modified: Wed, 21 Dec 2022 13:14:48 GMT  
		Size: 45.0 MB (44994592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5ddd0e7b8eeb5bc439dbae37cb86546355e99664fd68fe4239c8b9b11ec51b`  
		Last Modified: Wed, 21 Dec 2022 13:14:43 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830ef74f6bb15b98bebdb90fb766497e905d8fd61c68ffa5f88cf8971403c548`  
		Last Modified: Wed, 21 Dec 2022 13:14:56 GMT  
		Size: 112.9 MB (112940727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.18.6-sdk`

```console
$ docker pull dart@sha256:d0704c148be11dcfaf2221128ea1f200f19a5acce90396d73b4596b3fa318584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.18.6-sdk` - linux; amd64

```console
$ docker pull dart@sha256:f01f9640b241c8bcc9a9cafd7f9e907616e4417523ee956bbfcf938bb769e641
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271928321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f053d1795af04f470caba08091334ee9d6920c0baa93a66cfb26f732f01a770f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:15:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:15:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 02:15:49 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 02:15:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 02:15:49 GMT
WORKDIR /root
# Wed, 21 Dec 2022 02:16:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f93052e58e62ed85a7a429c69eefab2de9abcb0ea08cddf775756a369397cc4`  
		Last Modified: Wed, 21 Dec 2022 02:16:55 GMT  
		Size: 45.1 MB (45073057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a4a8d101c8f583489acf734e17554e63b1f2e68c38e36cce0ed2a1d38a5c76`  
		Last Modified: Wed, 21 Dec 2022 02:16:48 GMT  
		Size: 2.2 MB (2162025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cc094cc3bcdec2368b60911e81ea1a79086d5e291fca585ea0b324cd46ae82`  
		Last Modified: Wed, 21 Dec 2022 02:17:16 GMT  
		Size: 193.3 MB (193296296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.18.6-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2d360ee94083fb7a951c62a1983441bfb982a97e2e244cca61da6ec07cafdba8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180607509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7221d08b7e6217647bb8d51885062dd68aac7b60e6e0ed7a2c6ee9a68d19c228`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:00:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad75836ddeea1d435c6db7f3d2e2c8ba7ba9ff6ae8b495bb9d98be60e4fb93`  
		Last Modified: Sat, 17 Dec 2022 03:02:41 GMT  
		Size: 111.8 MB (111786221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.18.6-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:de509b6121dd3e5baa103d54cbb045b10d52da8356cd558d331b0f7c3d1c1820
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.5 MB (189542274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3573f824c49528f0db0955ef95287f5bb709564e08249e5c3d5b982fb9ff208`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:13:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:13:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 13:13:56 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 13:13:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 13:13:56 GMT
WORKDIR /root
# Wed, 21 Dec 2022 13:14:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdff8a458215716fab99b63df7cae1c0e12c9e84020634c3b6afd9512d7181f`  
		Last Modified: Wed, 21 Dec 2022 13:14:48 GMT  
		Size: 45.0 MB (44994592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5ddd0e7b8eeb5bc439dbae37cb86546355e99664fd68fe4239c8b9b11ec51b`  
		Last Modified: Wed, 21 Dec 2022 13:14:43 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830ef74f6bb15b98bebdb90fb766497e905d8fd61c68ffa5f88cf8971403c548`  
		Last Modified: Wed, 21 Dec 2022 13:14:56 GMT  
		Size: 112.9 MB (112940727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.19.0-444.2.beta`

```console
$ docker pull dart@sha256:ecabf6f9f0c4738b9eea2dab5a0e322cb632a81d34de5034e22f905016b3d041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.19.0-444.2.beta` - linux; amd64

```console
$ docker pull dart@sha256:5368aade04ddf999096a56d79629bce166a5e5440d2889249b1b3efbaa47c6f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308562878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab664c49507a64301945ed3dc650026e21b01875b15ff6003f313973529a259e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:15:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:15:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 02:15:49 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 02:15:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 02:15:49 GMT
WORKDIR /root
# Wed, 21 Dec 2022 02:16:26 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9454bfc7eeab61dd7d9b13a393c0c2978ee5a71a2059c687b1b2e8e31eef6740;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8b6d06901fda8603e9d0f91224f8d376ff10079a28491be33d84f5c9fbce816d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b03f47f26373873643e7e7ce85fad3b6fe0220d1707be774288e9b4f1d9beddf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-444.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f93052e58e62ed85a7a429c69eefab2de9abcb0ea08cddf775756a369397cc4`  
		Last Modified: Wed, 21 Dec 2022 02:16:55 GMT  
		Size: 45.1 MB (45073057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a4a8d101c8f583489acf734e17554e63b1f2e68c38e36cce0ed2a1d38a5c76`  
		Last Modified: Wed, 21 Dec 2022 02:16:48 GMT  
		Size: 2.2 MB (2162025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9aec8fc05d455ff04a143ff85da7ffda169c673e6c218fe2b2cdabfe88f1547`  
		Last Modified: Wed, 21 Dec 2022 02:18:16 GMT  
		Size: 229.9 MB (229930853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.19.0-444.2.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:452338a740655dc5f111eacd98bd9fe475240c22ce4860cd8d67f146691c9d88
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204941255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02650998c74ff6f59c8280b09af4742abd28677b579272501a2bb9a26ca3c9a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:01:19 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9454bfc7eeab61dd7d9b13a393c0c2978ee5a71a2059c687b1b2e8e31eef6740;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8b6d06901fda8603e9d0f91224f8d376ff10079a28491be33d84f5c9fbce816d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b03f47f26373873643e7e7ce85fad3b6fe0220d1707be774288e9b4f1d9beddf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-444.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dac8d78206a46493fc76fb9bac4a10aca73629c651f8adc104eaab397eb851`  
		Last Modified: Sat, 17 Dec 2022 03:03:42 GMT  
		Size: 136.1 MB (136119967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.19.0-444.2.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:76f417fe79ea9de500302c6887f52a663b0043f13b62c335a5647f240f1e7dd4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (214020191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41696576167fb72d0539b0df16d93d777f2ee59e7e3c487dfa57b59beddfd728`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:13:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:13:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 13:13:56 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 13:13:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 13:13:56 GMT
WORKDIR /root
# Wed, 21 Dec 2022 13:14:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9454bfc7eeab61dd7d9b13a393c0c2978ee5a71a2059c687b1b2e8e31eef6740;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8b6d06901fda8603e9d0f91224f8d376ff10079a28491be33d84f5c9fbce816d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b03f47f26373873643e7e7ce85fad3b6fe0220d1707be774288e9b4f1d9beddf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-444.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdff8a458215716fab99b63df7cae1c0e12c9e84020634c3b6afd9512d7181f`  
		Last Modified: Wed, 21 Dec 2022 13:14:48 GMT  
		Size: 45.0 MB (44994592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5ddd0e7b8eeb5bc439dbae37cb86546355e99664fd68fe4239c8b9b11ec51b`  
		Last Modified: Wed, 21 Dec 2022 13:14:43 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1af6ea270263751327e30da5bd83ea5aed5b3581dde2c8afeaf29b4f3bef7f8`  
		Last Modified: Wed, 21 Dec 2022 13:15:38 GMT  
		Size: 137.4 MB (137418644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.19.0-444.2.beta-sdk`

```console
$ docker pull dart@sha256:ecabf6f9f0c4738b9eea2dab5a0e322cb632a81d34de5034e22f905016b3d041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.19.0-444.2.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:5368aade04ddf999096a56d79629bce166a5e5440d2889249b1b3efbaa47c6f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308562878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab664c49507a64301945ed3dc650026e21b01875b15ff6003f313973529a259e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:15:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:15:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 02:15:49 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 02:15:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 02:15:49 GMT
WORKDIR /root
# Wed, 21 Dec 2022 02:16:26 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9454bfc7eeab61dd7d9b13a393c0c2978ee5a71a2059c687b1b2e8e31eef6740;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8b6d06901fda8603e9d0f91224f8d376ff10079a28491be33d84f5c9fbce816d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b03f47f26373873643e7e7ce85fad3b6fe0220d1707be774288e9b4f1d9beddf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-444.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f93052e58e62ed85a7a429c69eefab2de9abcb0ea08cddf775756a369397cc4`  
		Last Modified: Wed, 21 Dec 2022 02:16:55 GMT  
		Size: 45.1 MB (45073057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a4a8d101c8f583489acf734e17554e63b1f2e68c38e36cce0ed2a1d38a5c76`  
		Last Modified: Wed, 21 Dec 2022 02:16:48 GMT  
		Size: 2.2 MB (2162025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9aec8fc05d455ff04a143ff85da7ffda169c673e6c218fe2b2cdabfe88f1547`  
		Last Modified: Wed, 21 Dec 2022 02:18:16 GMT  
		Size: 229.9 MB (229930853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.19.0-444.2.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:452338a740655dc5f111eacd98bd9fe475240c22ce4860cd8d67f146691c9d88
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204941255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02650998c74ff6f59c8280b09af4742abd28677b579272501a2bb9a26ca3c9a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:01:19 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9454bfc7eeab61dd7d9b13a393c0c2978ee5a71a2059c687b1b2e8e31eef6740;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8b6d06901fda8603e9d0f91224f8d376ff10079a28491be33d84f5c9fbce816d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b03f47f26373873643e7e7ce85fad3b6fe0220d1707be774288e9b4f1d9beddf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-444.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dac8d78206a46493fc76fb9bac4a10aca73629c651f8adc104eaab397eb851`  
		Last Modified: Sat, 17 Dec 2022 03:03:42 GMT  
		Size: 136.1 MB (136119967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.19.0-444.2.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:76f417fe79ea9de500302c6887f52a663b0043f13b62c335a5647f240f1e7dd4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (214020191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41696576167fb72d0539b0df16d93d777f2ee59e7e3c487dfa57b59beddfd728`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:13:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:13:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 13:13:56 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 13:13:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 13:13:56 GMT
WORKDIR /root
# Wed, 21 Dec 2022 13:14:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9454bfc7eeab61dd7d9b13a393c0c2978ee5a71a2059c687b1b2e8e31eef6740;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8b6d06901fda8603e9d0f91224f8d376ff10079a28491be33d84f5c9fbce816d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b03f47f26373873643e7e7ce85fad3b6fe0220d1707be774288e9b4f1d9beddf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-444.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdff8a458215716fab99b63df7cae1c0e12c9e84020634c3b6afd9512d7181f`  
		Last Modified: Wed, 21 Dec 2022 13:14:48 GMT  
		Size: 45.0 MB (44994592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5ddd0e7b8eeb5bc439dbae37cb86546355e99664fd68fe4239c8b9b11ec51b`  
		Last Modified: Wed, 21 Dec 2022 13:14:43 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1af6ea270263751327e30da5bd83ea5aed5b3581dde2c8afeaf29b4f3bef7f8`  
		Last Modified: Wed, 21 Dec 2022 13:15:38 GMT  
		Size: 137.4 MB (137418644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta`

```console
$ docker pull dart@sha256:ecabf6f9f0c4738b9eea2dab5a0e322cb632a81d34de5034e22f905016b3d041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:5368aade04ddf999096a56d79629bce166a5e5440d2889249b1b3efbaa47c6f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308562878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab664c49507a64301945ed3dc650026e21b01875b15ff6003f313973529a259e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:15:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:15:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 02:15:49 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 02:15:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 02:15:49 GMT
WORKDIR /root
# Wed, 21 Dec 2022 02:16:26 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9454bfc7eeab61dd7d9b13a393c0c2978ee5a71a2059c687b1b2e8e31eef6740;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8b6d06901fda8603e9d0f91224f8d376ff10079a28491be33d84f5c9fbce816d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b03f47f26373873643e7e7ce85fad3b6fe0220d1707be774288e9b4f1d9beddf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-444.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f93052e58e62ed85a7a429c69eefab2de9abcb0ea08cddf775756a369397cc4`  
		Last Modified: Wed, 21 Dec 2022 02:16:55 GMT  
		Size: 45.1 MB (45073057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a4a8d101c8f583489acf734e17554e63b1f2e68c38e36cce0ed2a1d38a5c76`  
		Last Modified: Wed, 21 Dec 2022 02:16:48 GMT  
		Size: 2.2 MB (2162025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9aec8fc05d455ff04a143ff85da7ffda169c673e6c218fe2b2cdabfe88f1547`  
		Last Modified: Wed, 21 Dec 2022 02:18:16 GMT  
		Size: 229.9 MB (229930853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:452338a740655dc5f111eacd98bd9fe475240c22ce4860cd8d67f146691c9d88
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204941255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02650998c74ff6f59c8280b09af4742abd28677b579272501a2bb9a26ca3c9a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:01:19 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9454bfc7eeab61dd7d9b13a393c0c2978ee5a71a2059c687b1b2e8e31eef6740;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8b6d06901fda8603e9d0f91224f8d376ff10079a28491be33d84f5c9fbce816d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b03f47f26373873643e7e7ce85fad3b6fe0220d1707be774288e9b4f1d9beddf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-444.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dac8d78206a46493fc76fb9bac4a10aca73629c651f8adc104eaab397eb851`  
		Last Modified: Sat, 17 Dec 2022 03:03:42 GMT  
		Size: 136.1 MB (136119967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:76f417fe79ea9de500302c6887f52a663b0043f13b62c335a5647f240f1e7dd4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (214020191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41696576167fb72d0539b0df16d93d777f2ee59e7e3c487dfa57b59beddfd728`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:13:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:13:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 13:13:56 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 13:13:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 13:13:56 GMT
WORKDIR /root
# Wed, 21 Dec 2022 13:14:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9454bfc7eeab61dd7d9b13a393c0c2978ee5a71a2059c687b1b2e8e31eef6740;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8b6d06901fda8603e9d0f91224f8d376ff10079a28491be33d84f5c9fbce816d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b03f47f26373873643e7e7ce85fad3b6fe0220d1707be774288e9b4f1d9beddf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-444.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdff8a458215716fab99b63df7cae1c0e12c9e84020634c3b6afd9512d7181f`  
		Last Modified: Wed, 21 Dec 2022 13:14:48 GMT  
		Size: 45.0 MB (44994592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5ddd0e7b8eeb5bc439dbae37cb86546355e99664fd68fe4239c8b9b11ec51b`  
		Last Modified: Wed, 21 Dec 2022 13:14:43 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1af6ea270263751327e30da5bd83ea5aed5b3581dde2c8afeaf29b4f3bef7f8`  
		Last Modified: Wed, 21 Dec 2022 13:15:38 GMT  
		Size: 137.4 MB (137418644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:ecabf6f9f0c4738b9eea2dab5a0e322cb632a81d34de5034e22f905016b3d041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:5368aade04ddf999096a56d79629bce166a5e5440d2889249b1b3efbaa47c6f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308562878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab664c49507a64301945ed3dc650026e21b01875b15ff6003f313973529a259e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:15:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:15:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 02:15:49 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 02:15:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 02:15:49 GMT
WORKDIR /root
# Wed, 21 Dec 2022 02:16:26 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9454bfc7eeab61dd7d9b13a393c0c2978ee5a71a2059c687b1b2e8e31eef6740;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8b6d06901fda8603e9d0f91224f8d376ff10079a28491be33d84f5c9fbce816d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b03f47f26373873643e7e7ce85fad3b6fe0220d1707be774288e9b4f1d9beddf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-444.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f93052e58e62ed85a7a429c69eefab2de9abcb0ea08cddf775756a369397cc4`  
		Last Modified: Wed, 21 Dec 2022 02:16:55 GMT  
		Size: 45.1 MB (45073057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a4a8d101c8f583489acf734e17554e63b1f2e68c38e36cce0ed2a1d38a5c76`  
		Last Modified: Wed, 21 Dec 2022 02:16:48 GMT  
		Size: 2.2 MB (2162025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9aec8fc05d455ff04a143ff85da7ffda169c673e6c218fe2b2cdabfe88f1547`  
		Last Modified: Wed, 21 Dec 2022 02:18:16 GMT  
		Size: 229.9 MB (229930853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:452338a740655dc5f111eacd98bd9fe475240c22ce4860cd8d67f146691c9d88
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204941255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02650998c74ff6f59c8280b09af4742abd28677b579272501a2bb9a26ca3c9a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:01:19 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9454bfc7eeab61dd7d9b13a393c0c2978ee5a71a2059c687b1b2e8e31eef6740;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8b6d06901fda8603e9d0f91224f8d376ff10079a28491be33d84f5c9fbce816d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b03f47f26373873643e7e7ce85fad3b6fe0220d1707be774288e9b4f1d9beddf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-444.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dac8d78206a46493fc76fb9bac4a10aca73629c651f8adc104eaab397eb851`  
		Last Modified: Sat, 17 Dec 2022 03:03:42 GMT  
		Size: 136.1 MB (136119967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:76f417fe79ea9de500302c6887f52a663b0043f13b62c335a5647f240f1e7dd4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (214020191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41696576167fb72d0539b0df16d93d777f2ee59e7e3c487dfa57b59beddfd728`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:13:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:13:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 13:13:56 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 13:13:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 13:13:56 GMT
WORKDIR /root
# Wed, 21 Dec 2022 13:14:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9454bfc7eeab61dd7d9b13a393c0c2978ee5a71a2059c687b1b2e8e31eef6740;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8b6d06901fda8603e9d0f91224f8d376ff10079a28491be33d84f5c9fbce816d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b03f47f26373873643e7e7ce85fad3b6fe0220d1707be774288e9b4f1d9beddf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-444.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdff8a458215716fab99b63df7cae1c0e12c9e84020634c3b6afd9512d7181f`  
		Last Modified: Wed, 21 Dec 2022 13:14:48 GMT  
		Size: 45.0 MB (44994592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5ddd0e7b8eeb5bc439dbae37cb86546355e99664fd68fe4239c8b9b11ec51b`  
		Last Modified: Wed, 21 Dec 2022 13:14:43 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1af6ea270263751327e30da5bd83ea5aed5b3581dde2c8afeaf29b4f3bef7f8`  
		Last Modified: Wed, 21 Dec 2022 13:15:38 GMT  
		Size: 137.4 MB (137418644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:latest`

```console
$ docker pull dart@sha256:d0704c148be11dcfaf2221128ea1f200f19a5acce90396d73b4596b3fa318584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:f01f9640b241c8bcc9a9cafd7f9e907616e4417523ee956bbfcf938bb769e641
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271928321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f053d1795af04f470caba08091334ee9d6920c0baa93a66cfb26f732f01a770f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:15:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:15:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 02:15:49 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 02:15:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 02:15:49 GMT
WORKDIR /root
# Wed, 21 Dec 2022 02:16:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f93052e58e62ed85a7a429c69eefab2de9abcb0ea08cddf775756a369397cc4`  
		Last Modified: Wed, 21 Dec 2022 02:16:55 GMT  
		Size: 45.1 MB (45073057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a4a8d101c8f583489acf734e17554e63b1f2e68c38e36cce0ed2a1d38a5c76`  
		Last Modified: Wed, 21 Dec 2022 02:16:48 GMT  
		Size: 2.2 MB (2162025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cc094cc3bcdec2368b60911e81ea1a79086d5e291fca585ea0b324cd46ae82`  
		Last Modified: Wed, 21 Dec 2022 02:17:16 GMT  
		Size: 193.3 MB (193296296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:2d360ee94083fb7a951c62a1983441bfb982a97e2e244cca61da6ec07cafdba8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180607509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7221d08b7e6217647bb8d51885062dd68aac7b60e6e0ed7a2c6ee9a68d19c228`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:00:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad75836ddeea1d435c6db7f3d2e2c8ba7ba9ff6ae8b495bb9d98be60e4fb93`  
		Last Modified: Sat, 17 Dec 2022 03:02:41 GMT  
		Size: 111.8 MB (111786221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:de509b6121dd3e5baa103d54cbb045b10d52da8356cd558d331b0f7c3d1c1820
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.5 MB (189542274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3573f824c49528f0db0955ef95287f5bb709564e08249e5c3d5b982fb9ff208`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:13:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:13:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 13:13:56 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 13:13:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 13:13:56 GMT
WORKDIR /root
# Wed, 21 Dec 2022 13:14:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdff8a458215716fab99b63df7cae1c0e12c9e84020634c3b6afd9512d7181f`  
		Last Modified: Wed, 21 Dec 2022 13:14:48 GMT  
		Size: 45.0 MB (44994592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5ddd0e7b8eeb5bc439dbae37cb86546355e99664fd68fe4239c8b9b11ec51b`  
		Last Modified: Wed, 21 Dec 2022 13:14:43 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830ef74f6bb15b98bebdb90fb766497e905d8fd61c68ffa5f88cf8971403c548`  
		Last Modified: Wed, 21 Dec 2022 13:14:56 GMT  
		Size: 112.9 MB (112940727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:sdk`

```console
$ docker pull dart@sha256:d0704c148be11dcfaf2221128ea1f200f19a5acce90396d73b4596b3fa318584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:f01f9640b241c8bcc9a9cafd7f9e907616e4417523ee956bbfcf938bb769e641
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271928321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f053d1795af04f470caba08091334ee9d6920c0baa93a66cfb26f732f01a770f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:15:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:15:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 02:15:49 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 02:15:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 02:15:49 GMT
WORKDIR /root
# Wed, 21 Dec 2022 02:16:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f93052e58e62ed85a7a429c69eefab2de9abcb0ea08cddf775756a369397cc4`  
		Last Modified: Wed, 21 Dec 2022 02:16:55 GMT  
		Size: 45.1 MB (45073057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a4a8d101c8f583489acf734e17554e63b1f2e68c38e36cce0ed2a1d38a5c76`  
		Last Modified: Wed, 21 Dec 2022 02:16:48 GMT  
		Size: 2.2 MB (2162025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cc094cc3bcdec2368b60911e81ea1a79086d5e291fca585ea0b324cd46ae82`  
		Last Modified: Wed, 21 Dec 2022 02:17:16 GMT  
		Size: 193.3 MB (193296296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2d360ee94083fb7a951c62a1983441bfb982a97e2e244cca61da6ec07cafdba8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180607509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7221d08b7e6217647bb8d51885062dd68aac7b60e6e0ed7a2c6ee9a68d19c228`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:00:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad75836ddeea1d435c6db7f3d2e2c8ba7ba9ff6ae8b495bb9d98be60e4fb93`  
		Last Modified: Sat, 17 Dec 2022 03:02:41 GMT  
		Size: 111.8 MB (111786221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:de509b6121dd3e5baa103d54cbb045b10d52da8356cd558d331b0f7c3d1c1820
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.5 MB (189542274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3573f824c49528f0db0955ef95287f5bb709564e08249e5c3d5b982fb9ff208`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:13:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:13:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 13:13:56 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 13:13:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 13:13:56 GMT
WORKDIR /root
# Wed, 21 Dec 2022 13:14:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdff8a458215716fab99b63df7cae1c0e12c9e84020634c3b6afd9512d7181f`  
		Last Modified: Wed, 21 Dec 2022 13:14:48 GMT  
		Size: 45.0 MB (44994592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5ddd0e7b8eeb5bc439dbae37cb86546355e99664fd68fe4239c8b9b11ec51b`  
		Last Modified: Wed, 21 Dec 2022 13:14:43 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830ef74f6bb15b98bebdb90fb766497e905d8fd61c68ffa5f88cf8971403c548`  
		Last Modified: Wed, 21 Dec 2022 13:14:56 GMT  
		Size: 112.9 MB (112940727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable`

```console
$ docker pull dart@sha256:d0704c148be11dcfaf2221128ea1f200f19a5acce90396d73b4596b3fa318584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:f01f9640b241c8bcc9a9cafd7f9e907616e4417523ee956bbfcf938bb769e641
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271928321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f053d1795af04f470caba08091334ee9d6920c0baa93a66cfb26f732f01a770f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:15:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:15:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 02:15:49 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 02:15:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 02:15:49 GMT
WORKDIR /root
# Wed, 21 Dec 2022 02:16:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f93052e58e62ed85a7a429c69eefab2de9abcb0ea08cddf775756a369397cc4`  
		Last Modified: Wed, 21 Dec 2022 02:16:55 GMT  
		Size: 45.1 MB (45073057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a4a8d101c8f583489acf734e17554e63b1f2e68c38e36cce0ed2a1d38a5c76`  
		Last Modified: Wed, 21 Dec 2022 02:16:48 GMT  
		Size: 2.2 MB (2162025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cc094cc3bcdec2368b60911e81ea1a79086d5e291fca585ea0b324cd46ae82`  
		Last Modified: Wed, 21 Dec 2022 02:17:16 GMT  
		Size: 193.3 MB (193296296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:2d360ee94083fb7a951c62a1983441bfb982a97e2e244cca61da6ec07cafdba8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180607509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7221d08b7e6217647bb8d51885062dd68aac7b60e6e0ed7a2c6ee9a68d19c228`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:00:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad75836ddeea1d435c6db7f3d2e2c8ba7ba9ff6ae8b495bb9d98be60e4fb93`  
		Last Modified: Sat, 17 Dec 2022 03:02:41 GMT  
		Size: 111.8 MB (111786221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:de509b6121dd3e5baa103d54cbb045b10d52da8356cd558d331b0f7c3d1c1820
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.5 MB (189542274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3573f824c49528f0db0955ef95287f5bb709564e08249e5c3d5b982fb9ff208`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:13:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:13:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 13:13:56 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 13:13:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 13:13:56 GMT
WORKDIR /root
# Wed, 21 Dec 2022 13:14:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdff8a458215716fab99b63df7cae1c0e12c9e84020634c3b6afd9512d7181f`  
		Last Modified: Wed, 21 Dec 2022 13:14:48 GMT  
		Size: 45.0 MB (44994592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5ddd0e7b8eeb5bc439dbae37cb86546355e99664fd68fe4239c8b9b11ec51b`  
		Last Modified: Wed, 21 Dec 2022 13:14:43 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830ef74f6bb15b98bebdb90fb766497e905d8fd61c68ffa5f88cf8971403c548`  
		Last Modified: Wed, 21 Dec 2022 13:14:56 GMT  
		Size: 112.9 MB (112940727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:d0704c148be11dcfaf2221128ea1f200f19a5acce90396d73b4596b3fa318584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:f01f9640b241c8bcc9a9cafd7f9e907616e4417523ee956bbfcf938bb769e641
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271928321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f053d1795af04f470caba08091334ee9d6920c0baa93a66cfb26f732f01a770f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:15:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:15:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 02:15:49 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 02:15:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 02:15:49 GMT
WORKDIR /root
# Wed, 21 Dec 2022 02:16:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f93052e58e62ed85a7a429c69eefab2de9abcb0ea08cddf775756a369397cc4`  
		Last Modified: Wed, 21 Dec 2022 02:16:55 GMT  
		Size: 45.1 MB (45073057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a4a8d101c8f583489acf734e17554e63b1f2e68c38e36cce0ed2a1d38a5c76`  
		Last Modified: Wed, 21 Dec 2022 02:16:48 GMT  
		Size: 2.2 MB (2162025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cc094cc3bcdec2368b60911e81ea1a79086d5e291fca585ea0b324cd46ae82`  
		Last Modified: Wed, 21 Dec 2022 02:17:16 GMT  
		Size: 193.3 MB (193296296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2d360ee94083fb7a951c62a1983441bfb982a97e2e244cca61da6ec07cafdba8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180607509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7221d08b7e6217647bb8d51885062dd68aac7b60e6e0ed7a2c6ee9a68d19c228`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:00:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad75836ddeea1d435c6db7f3d2e2c8ba7ba9ff6ae8b495bb9d98be60e4fb93`  
		Last Modified: Sat, 17 Dec 2022 03:02:41 GMT  
		Size: 111.8 MB (111786221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:de509b6121dd3e5baa103d54cbb045b10d52da8356cd558d331b0f7c3d1c1820
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.5 MB (189542274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3573f824c49528f0db0955ef95287f5bb709564e08249e5c3d5b982fb9ff208`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:13:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:13:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 21 Dec 2022 13:13:56 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 21 Dec 2022 13:13:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 13:13:56 GMT
WORKDIR /root
# Wed, 21 Dec 2022 13:14:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdff8a458215716fab99b63df7cae1c0e12c9e84020634c3b6afd9512d7181f`  
		Last Modified: Wed, 21 Dec 2022 13:14:48 GMT  
		Size: 45.0 MB (44994592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5ddd0e7b8eeb5bc439dbae37cb86546355e99664fd68fe4239c8b9b11ec51b`  
		Last Modified: Wed, 21 Dec 2022 13:14:43 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830ef74f6bb15b98bebdb90fb766497e905d8fd61c68ffa5f88cf8971403c548`  
		Last Modified: Wed, 21 Dec 2022 13:14:56 GMT  
		Size: 112.9 MB (112940727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
