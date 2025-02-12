<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.7`](#dart37)
-	[`dart:3.7-sdk`](#dart37-sdk)
-	[`dart:3.7.0`](#dart370)
-	[`dart:3.7.0-sdk`](#dart370-sdk)
-	[`dart:3.8.0-70.1.beta`](#dart380-701beta)
-	[`dart:3.8.0-70.1.beta-sdk`](#dart380-701beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:7a6a4ad2560e46cb6979bd73f46edec0fa7bc092146f5fafefdf3c6568a77e75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3` - linux; amd64

```console
$ docker pull dart@sha256:553d8f8fc187ab31ad8f8ed9c4722c812057607e10a7dc5d4bb7d7e89def2c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312140840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3495d6c4d34ccf3d7457b9ecdfc1cc526891f9f4f09e260924d7e9915832923`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0785300a74e92d61d24e3d60a87edaff62d5ede8e74f2e8368f0c52408c49cee`  
		Last Modified: Tue, 04 Feb 2025 19:33:06 GMT  
		Size: 54.9 MB (54906742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9859598bb5e58e0449dd2866c56d84cc61eb6220a6b0508aa6717600b468fda`  
		Last Modified: Tue, 04 Feb 2025 19:33:05 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca07202c9e54f4fe2ceb63a5856929c2c74bd045a48581925abbaa393f8bba`  
		Last Modified: Tue, 04 Feb 2025 19:33:10 GMT  
		Size: 227.2 MB (227224845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:1ce94f4cc12a1678ea21e42b3970f8b3f1723599e5fd7ef168d772be9205601c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed10b94ea5d6396292c54f541f7004b4390ccf05184e6229a761784f235ff72`

```dockerfile
```

-	Layers:
	-	`sha256:e56081c707bee6a58dc1960a59c9511d6fb5dfce8beb6b34713ee777d1b2169e`  
		Last Modified: Tue, 04 Feb 2025 19:33:04 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:7797b06cd30bd8a160767cbe6fee899b15db87da3a9777973ec31ceda9b057a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210416806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461a879b8a85f626cfe3e1a0db73e6ec5105d069069fa379ce6463800bc2af47`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97e0e5b495d23129757e928035e502f9ddc2460eaed33276b37e02cf4d5d6b7`  
		Last Modified: Wed, 05 Feb 2025 00:32:54 GMT  
		Size: 49.6 MB (49561589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935d89e90625c93fe0c019b8eaa9ebdf9ae1648df3dd75648c4687904d513269`  
		Last Modified: Wed, 05 Feb 2025 00:32:49 GMT  
		Size: 1.2 MB (1221679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bfe1acf82982460382ed78cf98b547e6e9b40324f457c1571b2d571842cf74`  
		Last Modified: Wed, 05 Feb 2025 00:32:53 GMT  
		Size: 135.7 MB (135718970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:024d3e73e45c4f8dd09498b03d39f42b10bba4950399b3320efe8ad87ca6ccd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4641dd7e7ec16c32d8e4ee52dd011f48c7714faac661e635f286337ac4268415`

```dockerfile
```

-	Layers:
	-	`sha256:0e13cf82f02511e718e14dc6bf5660543131b00ac836e43e50cd9da81816320e`  
		Last Modified: Wed, 05 Feb 2025 00:32:49 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:89acde2d251bf0a8c3ca173ba87571032ad3a58fc93a1198ebd57e865ee7f9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310590748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3781eea0f6b74106a921e9040794478a29f4832511347a39d3b94da82664ef10`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b469059dc747afbabaede5f3655ecfab74835f657b78cb4e62b7d8d18f89b7`  
		Last Modified: Wed, 05 Feb 2025 01:54:01 GMT  
		Size: 54.7 MB (54678286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8373809adad2673f7ac23f4820372c9cbbde64064ea71582d97ac389e368447`  
		Last Modified: Wed, 05 Feb 2025 01:53:59 GMT  
		Size: 1.5 MB (1488032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5664a4f15612ecd4f60625e036d392d9a77a6faca9bb6ce9fd9fc38a4466b4f`  
		Last Modified: Wed, 05 Feb 2025 01:54:04 GMT  
		Size: 226.4 MB (226383517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:6f70eafe056ef47924115db62ec6b79ac2c6fb3b526e72f139977e448feb48af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54882f556af8ffeb5d1de63cefae5883d4f3aa74f39ab3151344510c9ee2cd7b`

```dockerfile
```

-	Layers:
	-	`sha256:c7468e7f4563819acb371538ac7b9e69b0450a97ccdc41deaf90c20e192c8866`  
		Last Modified: Wed, 05 Feb 2025 01:53:59 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:7a6a4ad2560e46cb6979bd73f46edec0fa7bc092146f5fafefdf3c6568a77e75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3-sdk` - linux; amd64

```console
$ docker pull dart@sha256:553d8f8fc187ab31ad8f8ed9c4722c812057607e10a7dc5d4bb7d7e89def2c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312140840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3495d6c4d34ccf3d7457b9ecdfc1cc526891f9f4f09e260924d7e9915832923`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0785300a74e92d61d24e3d60a87edaff62d5ede8e74f2e8368f0c52408c49cee`  
		Last Modified: Tue, 04 Feb 2025 19:33:06 GMT  
		Size: 54.9 MB (54906742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9859598bb5e58e0449dd2866c56d84cc61eb6220a6b0508aa6717600b468fda`  
		Last Modified: Tue, 04 Feb 2025 19:33:05 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca07202c9e54f4fe2ceb63a5856929c2c74bd045a48581925abbaa393f8bba`  
		Last Modified: Tue, 04 Feb 2025 19:33:10 GMT  
		Size: 227.2 MB (227224845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1ce94f4cc12a1678ea21e42b3970f8b3f1723599e5fd7ef168d772be9205601c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed10b94ea5d6396292c54f541f7004b4390ccf05184e6229a761784f235ff72`

```dockerfile
```

-	Layers:
	-	`sha256:e56081c707bee6a58dc1960a59c9511d6fb5dfce8beb6b34713ee777d1b2169e`  
		Last Modified: Tue, 04 Feb 2025 19:33:04 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:7797b06cd30bd8a160767cbe6fee899b15db87da3a9777973ec31ceda9b057a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210416806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461a879b8a85f626cfe3e1a0db73e6ec5105d069069fa379ce6463800bc2af47`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97e0e5b495d23129757e928035e502f9ddc2460eaed33276b37e02cf4d5d6b7`  
		Last Modified: Wed, 05 Feb 2025 00:32:54 GMT  
		Size: 49.6 MB (49561589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935d89e90625c93fe0c019b8eaa9ebdf9ae1648df3dd75648c4687904d513269`  
		Last Modified: Wed, 05 Feb 2025 00:32:49 GMT  
		Size: 1.2 MB (1221679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bfe1acf82982460382ed78cf98b547e6e9b40324f457c1571b2d571842cf74`  
		Last Modified: Wed, 05 Feb 2025 00:32:53 GMT  
		Size: 135.7 MB (135718970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:024d3e73e45c4f8dd09498b03d39f42b10bba4950399b3320efe8ad87ca6ccd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4641dd7e7ec16c32d8e4ee52dd011f48c7714faac661e635f286337ac4268415`

```dockerfile
```

-	Layers:
	-	`sha256:0e13cf82f02511e718e14dc6bf5660543131b00ac836e43e50cd9da81816320e`  
		Last Modified: Wed, 05 Feb 2025 00:32:49 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:89acde2d251bf0a8c3ca173ba87571032ad3a58fc93a1198ebd57e865ee7f9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310590748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3781eea0f6b74106a921e9040794478a29f4832511347a39d3b94da82664ef10`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b469059dc747afbabaede5f3655ecfab74835f657b78cb4e62b7d8d18f89b7`  
		Last Modified: Wed, 05 Feb 2025 01:54:01 GMT  
		Size: 54.7 MB (54678286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8373809adad2673f7ac23f4820372c9cbbde64064ea71582d97ac389e368447`  
		Last Modified: Wed, 05 Feb 2025 01:53:59 GMT  
		Size: 1.5 MB (1488032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5664a4f15612ecd4f60625e036d392d9a77a6faca9bb6ce9fd9fc38a4466b4f`  
		Last Modified: Wed, 05 Feb 2025 01:54:04 GMT  
		Size: 226.4 MB (226383517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6f70eafe056ef47924115db62ec6b79ac2c6fb3b526e72f139977e448feb48af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54882f556af8ffeb5d1de63cefae5883d4f3aa74f39ab3151344510c9ee2cd7b`

```dockerfile
```

-	Layers:
	-	`sha256:c7468e7f4563819acb371538ac7b9e69b0450a97ccdc41deaf90c20e192c8866`  
		Last Modified: Wed, 05 Feb 2025 01:53:59 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.7`

**does not exist** (yet?)

## `dart:3.7-sdk`

**does not exist** (yet?)

## `dart:3.7.0`

**does not exist** (yet?)

## `dart:3.7.0-sdk`

**does not exist** (yet?)

## `dart:3.8.0-70.1.beta`

**does not exist** (yet?)

## `dart:3.8.0-70.1.beta-sdk`

**does not exist** (yet?)

## `dart:beta`

```console
$ docker pull dart@sha256:1f12fbe83b6119b89adc809d522fb134653112113d8138c61f1adf3e00352fe1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:d14db02b1ddbad1227a94d523ac2692a2f9d63740d79930de41b28a058d6c3a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304940081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c592c1c68be72c2d6ecbd1b4122f51f0e5af18d4c92a45a9e973b32d92734e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 05 Feb 2025 12:06:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 05 Feb 2025 12:06:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Feb 2025 12:06:12 GMT
WORKDIR /root
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d6a462d124ac3b48c7a662b74a7502e734d00f51f815b2b311579c0078daccfd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=83562e543537e1a2410ecc9cbb048ef4cdaa94ab837787a3973aeed552f98fe8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d603f3a9020f64f59b68d8a746091c07afc38c8d8c23b0a75e21720a4da0bf4c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-323.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8d180a2a6fba525f6bd619575d9119dcf70231419419b82f262a31deb4170d`  
		Last Modified: Fri, 07 Feb 2025 01:28:38 GMT  
		Size: 54.9 MB (54906684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab1c62e6f1d8b54d7bfec96f9c4af7eaf5436894aecbd95abb271b5cde43d3d`  
		Last Modified: Fri, 07 Feb 2025 01:28:38 GMT  
		Size: 1.8 MB (1796897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6fb8af2a09fe17bd14d7d355fc84d14ba6749d73ee6730fb1b38f7442e42c0`  
		Last Modified: Fri, 07 Feb 2025 01:28:41 GMT  
		Size: 220.0 MB (220024165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:54fef2c13bd1d3f0f34cd044192249d55cec715a9d201c46b86c1edc46a020c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408c11a604dd86848dca581949a4eb197e37baf6270ee0608a02498ee64c14e6`

```dockerfile
```

-	Layers:
	-	`sha256:e8c72f97bbd24c33a08e9cd58023d27e293ed57372273c0ca60596bccaaa51a4`  
		Last Modified: Fri, 07 Feb 2025 01:28:38 GMT  
		Size: 17.9 KB (17910 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:314ee130f2d0d4784b0953032a591274f4380a953c332eda234212d04f09a241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226295420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4b7b4e08a9e7da1ac5b5745b7f5e08d25e7eb2b7793b4644d516d66c4c9948`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 05 Feb 2025 12:06:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 05 Feb 2025 12:06:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Feb 2025 12:06:12 GMT
WORKDIR /root
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d6a462d124ac3b48c7a662b74a7502e734d00f51f815b2b311579c0078daccfd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=83562e543537e1a2410ecc9cbb048ef4cdaa94ab837787a3973aeed552f98fe8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d603f3a9020f64f59b68d8a746091c07afc38c8d8c23b0a75e21720a4da0bf4c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-323.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8432744e96f8e3d90822a9a33b68fa65a289664ee5ac213442a4e52916168089`  
		Last Modified: Fri, 07 Feb 2025 03:20:03 GMT  
		Size: 49.6 MB (49561375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b710ff2c3b109be6fe938d2b7ab2cde4487ccf605b861e3cd5ee8c52d5cf0c25`  
		Last Modified: Fri, 07 Feb 2025 03:20:01 GMT  
		Size: 1.2 MB (1221678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc926946ea1a36a01be65a523b2a5078a83b9dd85bfe95c1f88c358a2bb8ab5b`  
		Last Modified: Fri, 07 Feb 2025 03:20:05 GMT  
		Size: 151.6 MB (151597799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:ff0f6766ff68f48f7da8e34067e2850bf351341b70e26f2691866a6f28656beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc9e105b97c94793aaf63fc99b3a5cbfee3ebbb770b87fc95ffdc1862b3dddf`

```dockerfile
```

-	Layers:
	-	`sha256:152db1344dfce1d3003af153661bd40bd62ea9de0f9518292345478228ac9246`  
		Last Modified: Fri, 07 Feb 2025 03:20:01 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:9ed40e8759ed4d725aca2f1ef654914423071eece09fa7e71f87b174da338a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303810824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:030406127a8d09d377de8e299f33eaa37c8ba78bc535338837ea2a2c4b4a3a6b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 05 Feb 2025 12:06:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 05 Feb 2025 12:06:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Feb 2025 12:06:12 GMT
WORKDIR /root
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d6a462d124ac3b48c7a662b74a7502e734d00f51f815b2b311579c0078daccfd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=83562e543537e1a2410ecc9cbb048ef4cdaa94ab837787a3973aeed552f98fe8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d603f3a9020f64f59b68d8a746091c07afc38c8d8c23b0a75e21720a4da0bf4c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-323.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58af1233d09bfad98bc960981cbc8881df170ee3f4214c372e90b53b6f7b450`  
		Last Modified: Fri, 07 Feb 2025 01:47:23 GMT  
		Size: 54.7 MB (54678608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc05226888eb43ebe8086d27d2f039bd73130b7ba6efb7a4bc0e04de959b9b4`  
		Last Modified: Fri, 07 Feb 2025 01:47:20 GMT  
		Size: 1.5 MB (1488034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0acb94c18e870be38c13c9d2dc0232b497146feb4f0d0b4c0094dc282f47fc`  
		Last Modified: Fri, 07 Feb 2025 01:47:26 GMT  
		Size: 219.6 MB (219603269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:6e208e683e396fb324c932275493fda4f2d22f58c313f1913501ec1600f55dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13da8768fc95c82e9496554677235ad34fc68d9418b39adeef381b3f2dc0a78`

```dockerfile
```

-	Layers:
	-	`sha256:add612a755844b5eb0a49a979c39630599b813f742553c8867b070fa0600655a`  
		Last Modified: Fri, 07 Feb 2025 01:47:20 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:1f12fbe83b6119b89adc809d522fb134653112113d8138c61f1adf3e00352fe1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:d14db02b1ddbad1227a94d523ac2692a2f9d63740d79930de41b28a058d6c3a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304940081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c592c1c68be72c2d6ecbd1b4122f51f0e5af18d4c92a45a9e973b32d92734e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 05 Feb 2025 12:06:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 05 Feb 2025 12:06:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Feb 2025 12:06:12 GMT
WORKDIR /root
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d6a462d124ac3b48c7a662b74a7502e734d00f51f815b2b311579c0078daccfd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=83562e543537e1a2410ecc9cbb048ef4cdaa94ab837787a3973aeed552f98fe8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d603f3a9020f64f59b68d8a746091c07afc38c8d8c23b0a75e21720a4da0bf4c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-323.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8d180a2a6fba525f6bd619575d9119dcf70231419419b82f262a31deb4170d`  
		Last Modified: Fri, 07 Feb 2025 01:28:38 GMT  
		Size: 54.9 MB (54906684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab1c62e6f1d8b54d7bfec96f9c4af7eaf5436894aecbd95abb271b5cde43d3d`  
		Last Modified: Fri, 07 Feb 2025 01:28:38 GMT  
		Size: 1.8 MB (1796897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6fb8af2a09fe17bd14d7d355fc84d14ba6749d73ee6730fb1b38f7442e42c0`  
		Last Modified: Fri, 07 Feb 2025 01:28:41 GMT  
		Size: 220.0 MB (220024165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:54fef2c13bd1d3f0f34cd044192249d55cec715a9d201c46b86c1edc46a020c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408c11a604dd86848dca581949a4eb197e37baf6270ee0608a02498ee64c14e6`

```dockerfile
```

-	Layers:
	-	`sha256:e8c72f97bbd24c33a08e9cd58023d27e293ed57372273c0ca60596bccaaa51a4`  
		Last Modified: Fri, 07 Feb 2025 01:28:38 GMT  
		Size: 17.9 KB (17910 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:314ee130f2d0d4784b0953032a591274f4380a953c332eda234212d04f09a241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226295420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4b7b4e08a9e7da1ac5b5745b7f5e08d25e7eb2b7793b4644d516d66c4c9948`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 05 Feb 2025 12:06:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 05 Feb 2025 12:06:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Feb 2025 12:06:12 GMT
WORKDIR /root
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d6a462d124ac3b48c7a662b74a7502e734d00f51f815b2b311579c0078daccfd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=83562e543537e1a2410ecc9cbb048ef4cdaa94ab837787a3973aeed552f98fe8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d603f3a9020f64f59b68d8a746091c07afc38c8d8c23b0a75e21720a4da0bf4c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-323.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8432744e96f8e3d90822a9a33b68fa65a289664ee5ac213442a4e52916168089`  
		Last Modified: Fri, 07 Feb 2025 03:20:03 GMT  
		Size: 49.6 MB (49561375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b710ff2c3b109be6fe938d2b7ab2cde4487ccf605b861e3cd5ee8c52d5cf0c25`  
		Last Modified: Fri, 07 Feb 2025 03:20:01 GMT  
		Size: 1.2 MB (1221678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc926946ea1a36a01be65a523b2a5078a83b9dd85bfe95c1f88c358a2bb8ab5b`  
		Last Modified: Fri, 07 Feb 2025 03:20:05 GMT  
		Size: 151.6 MB (151597799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ff0f6766ff68f48f7da8e34067e2850bf351341b70e26f2691866a6f28656beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc9e105b97c94793aaf63fc99b3a5cbfee3ebbb770b87fc95ffdc1862b3dddf`

```dockerfile
```

-	Layers:
	-	`sha256:152db1344dfce1d3003af153661bd40bd62ea9de0f9518292345478228ac9246`  
		Last Modified: Fri, 07 Feb 2025 03:20:01 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:9ed40e8759ed4d725aca2f1ef654914423071eece09fa7e71f87b174da338a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303810824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:030406127a8d09d377de8e299f33eaa37c8ba78bc535338837ea2a2c4b4a3a6b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 05 Feb 2025 12:06:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 05 Feb 2025 12:06:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Feb 2025 12:06:12 GMT
WORKDIR /root
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d6a462d124ac3b48c7a662b74a7502e734d00f51f815b2b311579c0078daccfd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=83562e543537e1a2410ecc9cbb048ef4cdaa94ab837787a3973aeed552f98fe8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d603f3a9020f64f59b68d8a746091c07afc38c8d8c23b0a75e21720a4da0bf4c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-323.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58af1233d09bfad98bc960981cbc8881df170ee3f4214c372e90b53b6f7b450`  
		Last Modified: Fri, 07 Feb 2025 01:47:23 GMT  
		Size: 54.7 MB (54678608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc05226888eb43ebe8086d27d2f039bd73130b7ba6efb7a4bc0e04de959b9b4`  
		Last Modified: Fri, 07 Feb 2025 01:47:20 GMT  
		Size: 1.5 MB (1488034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0acb94c18e870be38c13c9d2dc0232b497146feb4f0d0b4c0094dc282f47fc`  
		Last Modified: Fri, 07 Feb 2025 01:47:26 GMT  
		Size: 219.6 MB (219603269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6e208e683e396fb324c932275493fda4f2d22f58c313f1913501ec1600f55dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13da8768fc95c82e9496554677235ad34fc68d9418b39adeef381b3f2dc0a78`

```dockerfile
```

-	Layers:
	-	`sha256:add612a755844b5eb0a49a979c39630599b813f742553c8867b070fa0600655a`  
		Last Modified: Fri, 07 Feb 2025 01:47:20 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:7a6a4ad2560e46cb6979bd73f46edec0fa7bc092146f5fafefdf3c6568a77e75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:553d8f8fc187ab31ad8f8ed9c4722c812057607e10a7dc5d4bb7d7e89def2c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312140840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3495d6c4d34ccf3d7457b9ecdfc1cc526891f9f4f09e260924d7e9915832923`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0785300a74e92d61d24e3d60a87edaff62d5ede8e74f2e8368f0c52408c49cee`  
		Last Modified: Tue, 04 Feb 2025 19:33:06 GMT  
		Size: 54.9 MB (54906742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9859598bb5e58e0449dd2866c56d84cc61eb6220a6b0508aa6717600b468fda`  
		Last Modified: Tue, 04 Feb 2025 19:33:05 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca07202c9e54f4fe2ceb63a5856929c2c74bd045a48581925abbaa393f8bba`  
		Last Modified: Tue, 04 Feb 2025 19:33:10 GMT  
		Size: 227.2 MB (227224845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:1ce94f4cc12a1678ea21e42b3970f8b3f1723599e5fd7ef168d772be9205601c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed10b94ea5d6396292c54f541f7004b4390ccf05184e6229a761784f235ff72`

```dockerfile
```

-	Layers:
	-	`sha256:e56081c707bee6a58dc1960a59c9511d6fb5dfce8beb6b34713ee777d1b2169e`  
		Last Modified: Tue, 04 Feb 2025 19:33:04 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:7797b06cd30bd8a160767cbe6fee899b15db87da3a9777973ec31ceda9b057a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210416806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461a879b8a85f626cfe3e1a0db73e6ec5105d069069fa379ce6463800bc2af47`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97e0e5b495d23129757e928035e502f9ddc2460eaed33276b37e02cf4d5d6b7`  
		Last Modified: Wed, 05 Feb 2025 00:32:54 GMT  
		Size: 49.6 MB (49561589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935d89e90625c93fe0c019b8eaa9ebdf9ae1648df3dd75648c4687904d513269`  
		Last Modified: Wed, 05 Feb 2025 00:32:49 GMT  
		Size: 1.2 MB (1221679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bfe1acf82982460382ed78cf98b547e6e9b40324f457c1571b2d571842cf74`  
		Last Modified: Wed, 05 Feb 2025 00:32:53 GMT  
		Size: 135.7 MB (135718970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:024d3e73e45c4f8dd09498b03d39f42b10bba4950399b3320efe8ad87ca6ccd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4641dd7e7ec16c32d8e4ee52dd011f48c7714faac661e635f286337ac4268415`

```dockerfile
```

-	Layers:
	-	`sha256:0e13cf82f02511e718e14dc6bf5660543131b00ac836e43e50cd9da81816320e`  
		Last Modified: Wed, 05 Feb 2025 00:32:49 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:89acde2d251bf0a8c3ca173ba87571032ad3a58fc93a1198ebd57e865ee7f9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310590748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3781eea0f6b74106a921e9040794478a29f4832511347a39d3b94da82664ef10`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b469059dc747afbabaede5f3655ecfab74835f657b78cb4e62b7d8d18f89b7`  
		Last Modified: Wed, 05 Feb 2025 01:54:01 GMT  
		Size: 54.7 MB (54678286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8373809adad2673f7ac23f4820372c9cbbde64064ea71582d97ac389e368447`  
		Last Modified: Wed, 05 Feb 2025 01:53:59 GMT  
		Size: 1.5 MB (1488032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5664a4f15612ecd4f60625e036d392d9a77a6faca9bb6ce9fd9fc38a4466b4f`  
		Last Modified: Wed, 05 Feb 2025 01:54:04 GMT  
		Size: 226.4 MB (226383517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:6f70eafe056ef47924115db62ec6b79ac2c6fb3b526e72f139977e448feb48af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54882f556af8ffeb5d1de63cefae5883d4f3aa74f39ab3151344510c9ee2cd7b`

```dockerfile
```

-	Layers:
	-	`sha256:c7468e7f4563819acb371538ac7b9e69b0450a97ccdc41deaf90c20e192c8866`  
		Last Modified: Wed, 05 Feb 2025 01:53:59 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:7a6a4ad2560e46cb6979bd73f46edec0fa7bc092146f5fafefdf3c6568a77e75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:553d8f8fc187ab31ad8f8ed9c4722c812057607e10a7dc5d4bb7d7e89def2c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312140840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3495d6c4d34ccf3d7457b9ecdfc1cc526891f9f4f09e260924d7e9915832923`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0785300a74e92d61d24e3d60a87edaff62d5ede8e74f2e8368f0c52408c49cee`  
		Last Modified: Tue, 04 Feb 2025 19:33:06 GMT  
		Size: 54.9 MB (54906742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9859598bb5e58e0449dd2866c56d84cc61eb6220a6b0508aa6717600b468fda`  
		Last Modified: Tue, 04 Feb 2025 19:33:05 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca07202c9e54f4fe2ceb63a5856929c2c74bd045a48581925abbaa393f8bba`  
		Last Modified: Tue, 04 Feb 2025 19:33:10 GMT  
		Size: 227.2 MB (227224845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1ce94f4cc12a1678ea21e42b3970f8b3f1723599e5fd7ef168d772be9205601c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed10b94ea5d6396292c54f541f7004b4390ccf05184e6229a761784f235ff72`

```dockerfile
```

-	Layers:
	-	`sha256:e56081c707bee6a58dc1960a59c9511d6fb5dfce8beb6b34713ee777d1b2169e`  
		Last Modified: Tue, 04 Feb 2025 19:33:04 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:7797b06cd30bd8a160767cbe6fee899b15db87da3a9777973ec31ceda9b057a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210416806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461a879b8a85f626cfe3e1a0db73e6ec5105d069069fa379ce6463800bc2af47`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97e0e5b495d23129757e928035e502f9ddc2460eaed33276b37e02cf4d5d6b7`  
		Last Modified: Wed, 05 Feb 2025 00:32:54 GMT  
		Size: 49.6 MB (49561589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935d89e90625c93fe0c019b8eaa9ebdf9ae1648df3dd75648c4687904d513269`  
		Last Modified: Wed, 05 Feb 2025 00:32:49 GMT  
		Size: 1.2 MB (1221679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bfe1acf82982460382ed78cf98b547e6e9b40324f457c1571b2d571842cf74`  
		Last Modified: Wed, 05 Feb 2025 00:32:53 GMT  
		Size: 135.7 MB (135718970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:024d3e73e45c4f8dd09498b03d39f42b10bba4950399b3320efe8ad87ca6ccd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4641dd7e7ec16c32d8e4ee52dd011f48c7714faac661e635f286337ac4268415`

```dockerfile
```

-	Layers:
	-	`sha256:0e13cf82f02511e718e14dc6bf5660543131b00ac836e43e50cd9da81816320e`  
		Last Modified: Wed, 05 Feb 2025 00:32:49 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:89acde2d251bf0a8c3ca173ba87571032ad3a58fc93a1198ebd57e865ee7f9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310590748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3781eea0f6b74106a921e9040794478a29f4832511347a39d3b94da82664ef10`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b469059dc747afbabaede5f3655ecfab74835f657b78cb4e62b7d8d18f89b7`  
		Last Modified: Wed, 05 Feb 2025 01:54:01 GMT  
		Size: 54.7 MB (54678286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8373809adad2673f7ac23f4820372c9cbbde64064ea71582d97ac389e368447`  
		Last Modified: Wed, 05 Feb 2025 01:53:59 GMT  
		Size: 1.5 MB (1488032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5664a4f15612ecd4f60625e036d392d9a77a6faca9bb6ce9fd9fc38a4466b4f`  
		Last Modified: Wed, 05 Feb 2025 01:54:04 GMT  
		Size: 226.4 MB (226383517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6f70eafe056ef47924115db62ec6b79ac2c6fb3b526e72f139977e448feb48af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54882f556af8ffeb5d1de63cefae5883d4f3aa74f39ab3151344510c9ee2cd7b`

```dockerfile
```

-	Layers:
	-	`sha256:c7468e7f4563819acb371538ac7b9e69b0450a97ccdc41deaf90c20e192c8866`  
		Last Modified: Wed, 05 Feb 2025 01:53:59 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:7a6a4ad2560e46cb6979bd73f46edec0fa7bc092146f5fafefdf3c6568a77e75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:553d8f8fc187ab31ad8f8ed9c4722c812057607e10a7dc5d4bb7d7e89def2c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312140840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3495d6c4d34ccf3d7457b9ecdfc1cc526891f9f4f09e260924d7e9915832923`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0785300a74e92d61d24e3d60a87edaff62d5ede8e74f2e8368f0c52408c49cee`  
		Last Modified: Tue, 04 Feb 2025 19:33:06 GMT  
		Size: 54.9 MB (54906742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9859598bb5e58e0449dd2866c56d84cc61eb6220a6b0508aa6717600b468fda`  
		Last Modified: Tue, 04 Feb 2025 19:33:05 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca07202c9e54f4fe2ceb63a5856929c2c74bd045a48581925abbaa393f8bba`  
		Last Modified: Tue, 04 Feb 2025 19:33:10 GMT  
		Size: 227.2 MB (227224845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:1ce94f4cc12a1678ea21e42b3970f8b3f1723599e5fd7ef168d772be9205601c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed10b94ea5d6396292c54f541f7004b4390ccf05184e6229a761784f235ff72`

```dockerfile
```

-	Layers:
	-	`sha256:e56081c707bee6a58dc1960a59c9511d6fb5dfce8beb6b34713ee777d1b2169e`  
		Last Modified: Tue, 04 Feb 2025 19:33:04 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:7797b06cd30bd8a160767cbe6fee899b15db87da3a9777973ec31ceda9b057a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210416806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461a879b8a85f626cfe3e1a0db73e6ec5105d069069fa379ce6463800bc2af47`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97e0e5b495d23129757e928035e502f9ddc2460eaed33276b37e02cf4d5d6b7`  
		Last Modified: Wed, 05 Feb 2025 00:32:54 GMT  
		Size: 49.6 MB (49561589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935d89e90625c93fe0c019b8eaa9ebdf9ae1648df3dd75648c4687904d513269`  
		Last Modified: Wed, 05 Feb 2025 00:32:49 GMT  
		Size: 1.2 MB (1221679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bfe1acf82982460382ed78cf98b547e6e9b40324f457c1571b2d571842cf74`  
		Last Modified: Wed, 05 Feb 2025 00:32:53 GMT  
		Size: 135.7 MB (135718970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:024d3e73e45c4f8dd09498b03d39f42b10bba4950399b3320efe8ad87ca6ccd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4641dd7e7ec16c32d8e4ee52dd011f48c7714faac661e635f286337ac4268415`

```dockerfile
```

-	Layers:
	-	`sha256:0e13cf82f02511e718e14dc6bf5660543131b00ac836e43e50cd9da81816320e`  
		Last Modified: Wed, 05 Feb 2025 00:32:49 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:89acde2d251bf0a8c3ca173ba87571032ad3a58fc93a1198ebd57e865ee7f9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310590748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3781eea0f6b74106a921e9040794478a29f4832511347a39d3b94da82664ef10`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b469059dc747afbabaede5f3655ecfab74835f657b78cb4e62b7d8d18f89b7`  
		Last Modified: Wed, 05 Feb 2025 01:54:01 GMT  
		Size: 54.7 MB (54678286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8373809adad2673f7ac23f4820372c9cbbde64064ea71582d97ac389e368447`  
		Last Modified: Wed, 05 Feb 2025 01:53:59 GMT  
		Size: 1.5 MB (1488032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5664a4f15612ecd4f60625e036d392d9a77a6faca9bb6ce9fd9fc38a4466b4f`  
		Last Modified: Wed, 05 Feb 2025 01:54:04 GMT  
		Size: 226.4 MB (226383517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:6f70eafe056ef47924115db62ec6b79ac2c6fb3b526e72f139977e448feb48af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54882f556af8ffeb5d1de63cefae5883d4f3aa74f39ab3151344510c9ee2cd7b`

```dockerfile
```

-	Layers:
	-	`sha256:c7468e7f4563819acb371538ac7b9e69b0450a97ccdc41deaf90c20e192c8866`  
		Last Modified: Wed, 05 Feb 2025 01:53:59 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:7a6a4ad2560e46cb6979bd73f46edec0fa7bc092146f5fafefdf3c6568a77e75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:553d8f8fc187ab31ad8f8ed9c4722c812057607e10a7dc5d4bb7d7e89def2c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312140840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3495d6c4d34ccf3d7457b9ecdfc1cc526891f9f4f09e260924d7e9915832923`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0785300a74e92d61d24e3d60a87edaff62d5ede8e74f2e8368f0c52408c49cee`  
		Last Modified: Tue, 04 Feb 2025 19:33:06 GMT  
		Size: 54.9 MB (54906742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9859598bb5e58e0449dd2866c56d84cc61eb6220a6b0508aa6717600b468fda`  
		Last Modified: Tue, 04 Feb 2025 19:33:05 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca07202c9e54f4fe2ceb63a5856929c2c74bd045a48581925abbaa393f8bba`  
		Last Modified: Tue, 04 Feb 2025 19:33:10 GMT  
		Size: 227.2 MB (227224845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1ce94f4cc12a1678ea21e42b3970f8b3f1723599e5fd7ef168d772be9205601c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed10b94ea5d6396292c54f541f7004b4390ccf05184e6229a761784f235ff72`

```dockerfile
```

-	Layers:
	-	`sha256:e56081c707bee6a58dc1960a59c9511d6fb5dfce8beb6b34713ee777d1b2169e`  
		Last Modified: Tue, 04 Feb 2025 19:33:04 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:7797b06cd30bd8a160767cbe6fee899b15db87da3a9777973ec31ceda9b057a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210416806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461a879b8a85f626cfe3e1a0db73e6ec5105d069069fa379ce6463800bc2af47`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97e0e5b495d23129757e928035e502f9ddc2460eaed33276b37e02cf4d5d6b7`  
		Last Modified: Wed, 05 Feb 2025 00:32:54 GMT  
		Size: 49.6 MB (49561589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935d89e90625c93fe0c019b8eaa9ebdf9ae1648df3dd75648c4687904d513269`  
		Last Modified: Wed, 05 Feb 2025 00:32:49 GMT  
		Size: 1.2 MB (1221679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bfe1acf82982460382ed78cf98b547e6e9b40324f457c1571b2d571842cf74`  
		Last Modified: Wed, 05 Feb 2025 00:32:53 GMT  
		Size: 135.7 MB (135718970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:024d3e73e45c4f8dd09498b03d39f42b10bba4950399b3320efe8ad87ca6ccd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4641dd7e7ec16c32d8e4ee52dd011f48c7714faac661e635f286337ac4268415`

```dockerfile
```

-	Layers:
	-	`sha256:0e13cf82f02511e718e14dc6bf5660543131b00ac836e43e50cd9da81816320e`  
		Last Modified: Wed, 05 Feb 2025 00:32:49 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:89acde2d251bf0a8c3ca173ba87571032ad3a58fc93a1198ebd57e865ee7f9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310590748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3781eea0f6b74106a921e9040794478a29f4832511347a39d3b94da82664ef10`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b469059dc747afbabaede5f3655ecfab74835f657b78cb4e62b7d8d18f89b7`  
		Last Modified: Wed, 05 Feb 2025 01:54:01 GMT  
		Size: 54.7 MB (54678286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8373809adad2673f7ac23f4820372c9cbbde64064ea71582d97ac389e368447`  
		Last Modified: Wed, 05 Feb 2025 01:53:59 GMT  
		Size: 1.5 MB (1488032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5664a4f15612ecd4f60625e036d392d9a77a6faca9bb6ce9fd9fc38a4466b4f`  
		Last Modified: Wed, 05 Feb 2025 01:54:04 GMT  
		Size: 226.4 MB (226383517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6f70eafe056ef47924115db62ec6b79ac2c6fb3b526e72f139977e448feb48af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54882f556af8ffeb5d1de63cefae5883d4f3aa74f39ab3151344510c9ee2cd7b`

```dockerfile
```

-	Layers:
	-	`sha256:c7468e7f4563819acb371538ac7b9e69b0450a97ccdc41deaf90c20e192c8866`  
		Last Modified: Wed, 05 Feb 2025 01:53:59 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json
