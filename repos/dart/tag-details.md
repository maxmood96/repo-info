<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.7`](#dart37)
-	[`dart:3.7-sdk`](#dart37-sdk)
-	[`dart:3.7.2`](#dart372)
-	[`dart:3.7.2-sdk`](#dart372-sdk)
-	[`dart:3.8.0-171.2.beta`](#dart380-1712beta)
-	[`dart:3.8.0-171.2.beta-sdk`](#dart380-1712beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:5e209253ec4b60200808157d99f3b1399aade3d449dbad537edcd95d54e50965
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
$ docker pull dart@sha256:e7511450d0b8bbc00355012e911d058e982e8606a6c542b2b5d97b6b3a4e77ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305381719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0960803cd33ec18cf437a59477528d6a8ee32ae039f9692deb15657b0fe99eed`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Mar 2025 13:16:06 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 27 Mar 2025 13:16:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:16:06 GMT
WORKDIR /root
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679997ce086256ff83ecd067858ae7b3e78f0b23c25943535915494859cca1f8`  
		Last Modified: Tue, 08 Apr 2025 01:25:29 GMT  
		Size: 54.9 MB (54907945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a5f32ada0a0fcf930ede1717dd841fa3f5c6f64e8310bde9080529a41015b2`  
		Last Modified: Tue, 08 Apr 2025 01:25:28 GMT  
		Size: 1.8 MB (1785449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90f887541e2b4482dfd6c92ceb0527fc54d9b10614646e5da880ed99aee4dfb`  
		Last Modified: Tue, 08 Apr 2025 01:25:32 GMT  
		Size: 220.5 MB (220461034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:a32403c56f9affea98af96da7f0ac7ba283edeb324ff741aab0f44eaf7cfddf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf4f1d80d172369e0d24cef022c6c0d9e83e60f43c022780c93c3df51692977`

```dockerfile
```

-	Layers:
	-	`sha256:404bb1ddc2df517b6fee1f7c088a9571d5fc6e5a84529591d775bbb8c7a357e5`  
		Last Modified: Tue, 08 Apr 2025 01:25:28 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d9c927c152b2c3d87e3ac69afd6328f9831a2875f33dcc4cc4cd425c40f735b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226291105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2261335dcf37c21db7f023a0451fa4ecdbc75b1fb9d59b127dd7f060398ea7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c93b8fd21f16e455ea78d5bde6caa154201a29de8b46231a24c2add8c4617b`  
		Last Modified: Tue, 18 Mar 2025 06:31:14 GMT  
		Size: 49.6 MB (49561746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3c3c9f9d55928fead9f3a4da4831bf52da646fa70eeb43ecaec385a9c4b68d`  
		Last Modified: Tue, 18 Mar 2025 06:31:12 GMT  
		Size: 1.2 MB (1221938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce883cc8a1d5b91b14d7dc7d44b8107de304cef7c3c386149cc8d1e279ea9eb3`  
		Last Modified: Tue, 18 Mar 2025 06:31:16 GMT  
		Size: 151.6 MB (151592301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:e2eaee0b4542bba459542c17bf1b54bc120ed38a3ae9188f880c7d56b26231a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2823625c0f31d59bcaa795a19cff381dadba16d0b7dbb878c6c5a9a027e6543d`

```dockerfile
```

-	Layers:
	-	`sha256:7c42669dfe6ff893492a04fdddf54c8fa268ce6053f36c27b30a7c4fd129d247`  
		Last Modified: Tue, 18 Mar 2025 06:31:12 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:fa9072f808cb3c8ac1230498ac721ca055d5667a5e4e7c7f45dcd21a5bb8a5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303837214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b765cccbabb6cd73309fa9fd557e2e1ae8ac1eb7f7a0885e675c7c43b259a882`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0e44317139d437e3a0030b2a5681351b64688c925cabaf26c463eae756097d`  
		Last Modified: Tue, 18 Mar 2025 05:32:15 GMT  
		Size: 54.7 MB (54678888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e6ea165b50c90409bcc2021c84bb757614ecf3c10c11a0c866f97673091e36`  
		Last Modified: Tue, 18 Mar 2025 05:32:13 GMT  
		Size: 1.5 MB (1488212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12a2d23e63fd0ca0f9c767ac72fe75b2ff092e16511e166c978d9ad000246b9`  
		Last Modified: Tue, 18 Mar 2025 05:32:18 GMT  
		Size: 219.6 MB (219626045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:6f95762d375ba3eeae8aad857d442e2c220ee8fb9d163d2094effe5e2b5caaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d52c0a42000c08e48c92bca0cb052efe5fe4c425c94f38928e03a760d35c27a`

```dockerfile
```

-	Layers:
	-	`sha256:417cb0c8593799bfc188df240164693386c9ddfaa96d2ab8b1617c6bc857bed2`  
		Last Modified: Tue, 18 Mar 2025 05:32:13 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:5e209253ec4b60200808157d99f3b1399aade3d449dbad537edcd95d54e50965
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
$ docker pull dart@sha256:e7511450d0b8bbc00355012e911d058e982e8606a6c542b2b5d97b6b3a4e77ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305381719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0960803cd33ec18cf437a59477528d6a8ee32ae039f9692deb15657b0fe99eed`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Mar 2025 13:16:06 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 27 Mar 2025 13:16:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:16:06 GMT
WORKDIR /root
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679997ce086256ff83ecd067858ae7b3e78f0b23c25943535915494859cca1f8`  
		Last Modified: Tue, 08 Apr 2025 01:25:29 GMT  
		Size: 54.9 MB (54907945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a5f32ada0a0fcf930ede1717dd841fa3f5c6f64e8310bde9080529a41015b2`  
		Last Modified: Tue, 08 Apr 2025 01:25:28 GMT  
		Size: 1.8 MB (1785449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90f887541e2b4482dfd6c92ceb0527fc54d9b10614646e5da880ed99aee4dfb`  
		Last Modified: Tue, 08 Apr 2025 01:25:32 GMT  
		Size: 220.5 MB (220461034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a32403c56f9affea98af96da7f0ac7ba283edeb324ff741aab0f44eaf7cfddf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf4f1d80d172369e0d24cef022c6c0d9e83e60f43c022780c93c3df51692977`

```dockerfile
```

-	Layers:
	-	`sha256:404bb1ddc2df517b6fee1f7c088a9571d5fc6e5a84529591d775bbb8c7a357e5`  
		Last Modified: Tue, 08 Apr 2025 01:25:28 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d9c927c152b2c3d87e3ac69afd6328f9831a2875f33dcc4cc4cd425c40f735b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226291105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2261335dcf37c21db7f023a0451fa4ecdbc75b1fb9d59b127dd7f060398ea7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c93b8fd21f16e455ea78d5bde6caa154201a29de8b46231a24c2add8c4617b`  
		Last Modified: Tue, 18 Mar 2025 06:31:14 GMT  
		Size: 49.6 MB (49561746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3c3c9f9d55928fead9f3a4da4831bf52da646fa70eeb43ecaec385a9c4b68d`  
		Last Modified: Tue, 18 Mar 2025 06:31:12 GMT  
		Size: 1.2 MB (1221938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce883cc8a1d5b91b14d7dc7d44b8107de304cef7c3c386149cc8d1e279ea9eb3`  
		Last Modified: Tue, 18 Mar 2025 06:31:16 GMT  
		Size: 151.6 MB (151592301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e2eaee0b4542bba459542c17bf1b54bc120ed38a3ae9188f880c7d56b26231a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2823625c0f31d59bcaa795a19cff381dadba16d0b7dbb878c6c5a9a027e6543d`

```dockerfile
```

-	Layers:
	-	`sha256:7c42669dfe6ff893492a04fdddf54c8fa268ce6053f36c27b30a7c4fd129d247`  
		Last Modified: Tue, 18 Mar 2025 06:31:12 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:fa9072f808cb3c8ac1230498ac721ca055d5667a5e4e7c7f45dcd21a5bb8a5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303837214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b765cccbabb6cd73309fa9fd557e2e1ae8ac1eb7f7a0885e675c7c43b259a882`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0e44317139d437e3a0030b2a5681351b64688c925cabaf26c463eae756097d`  
		Last Modified: Tue, 18 Mar 2025 05:32:15 GMT  
		Size: 54.7 MB (54678888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e6ea165b50c90409bcc2021c84bb757614ecf3c10c11a0c866f97673091e36`  
		Last Modified: Tue, 18 Mar 2025 05:32:13 GMT  
		Size: 1.5 MB (1488212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12a2d23e63fd0ca0f9c767ac72fe75b2ff092e16511e166c978d9ad000246b9`  
		Last Modified: Tue, 18 Mar 2025 05:32:18 GMT  
		Size: 219.6 MB (219626045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6f95762d375ba3eeae8aad857d442e2c220ee8fb9d163d2094effe5e2b5caaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d52c0a42000c08e48c92bca0cb052efe5fe4c425c94f38928e03a760d35c27a`

```dockerfile
```

-	Layers:
	-	`sha256:417cb0c8593799bfc188df240164693386c9ddfaa96d2ab8b1617c6bc857bed2`  
		Last Modified: Tue, 18 Mar 2025 05:32:13 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.7`

```console
$ docker pull dart@sha256:5e209253ec4b60200808157d99f3b1399aade3d449dbad537edcd95d54e50965
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.7` - linux; amd64

```console
$ docker pull dart@sha256:e7511450d0b8bbc00355012e911d058e982e8606a6c542b2b5d97b6b3a4e77ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305381719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0960803cd33ec18cf437a59477528d6a8ee32ae039f9692deb15657b0fe99eed`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Mar 2025 13:16:06 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 27 Mar 2025 13:16:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:16:06 GMT
WORKDIR /root
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679997ce086256ff83ecd067858ae7b3e78f0b23c25943535915494859cca1f8`  
		Last Modified: Tue, 08 Apr 2025 01:25:29 GMT  
		Size: 54.9 MB (54907945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a5f32ada0a0fcf930ede1717dd841fa3f5c6f64e8310bde9080529a41015b2`  
		Last Modified: Tue, 08 Apr 2025 01:25:28 GMT  
		Size: 1.8 MB (1785449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90f887541e2b4482dfd6c92ceb0527fc54d9b10614646e5da880ed99aee4dfb`  
		Last Modified: Tue, 08 Apr 2025 01:25:32 GMT  
		Size: 220.5 MB (220461034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7` - unknown; unknown

```console
$ docker pull dart@sha256:a32403c56f9affea98af96da7f0ac7ba283edeb324ff741aab0f44eaf7cfddf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf4f1d80d172369e0d24cef022c6c0d9e83e60f43c022780c93c3df51692977`

```dockerfile
```

-	Layers:
	-	`sha256:404bb1ddc2df517b6fee1f7c088a9571d5fc6e5a84529591d775bbb8c7a357e5`  
		Last Modified: Tue, 08 Apr 2025 01:25:28 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d9c927c152b2c3d87e3ac69afd6328f9831a2875f33dcc4cc4cd425c40f735b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226291105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2261335dcf37c21db7f023a0451fa4ecdbc75b1fb9d59b127dd7f060398ea7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c93b8fd21f16e455ea78d5bde6caa154201a29de8b46231a24c2add8c4617b`  
		Last Modified: Tue, 18 Mar 2025 06:31:14 GMT  
		Size: 49.6 MB (49561746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3c3c9f9d55928fead9f3a4da4831bf52da646fa70eeb43ecaec385a9c4b68d`  
		Last Modified: Tue, 18 Mar 2025 06:31:12 GMT  
		Size: 1.2 MB (1221938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce883cc8a1d5b91b14d7dc7d44b8107de304cef7c3c386149cc8d1e279ea9eb3`  
		Last Modified: Tue, 18 Mar 2025 06:31:16 GMT  
		Size: 151.6 MB (151592301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7` - unknown; unknown

```console
$ docker pull dart@sha256:e2eaee0b4542bba459542c17bf1b54bc120ed38a3ae9188f880c7d56b26231a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2823625c0f31d59bcaa795a19cff381dadba16d0b7dbb878c6c5a9a027e6543d`

```dockerfile
```

-	Layers:
	-	`sha256:7c42669dfe6ff893492a04fdddf54c8fa268ce6053f36c27b30a7c4fd129d247`  
		Last Modified: Tue, 18 Mar 2025 06:31:12 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:fa9072f808cb3c8ac1230498ac721ca055d5667a5e4e7c7f45dcd21a5bb8a5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303837214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b765cccbabb6cd73309fa9fd557e2e1ae8ac1eb7f7a0885e675c7c43b259a882`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0e44317139d437e3a0030b2a5681351b64688c925cabaf26c463eae756097d`  
		Last Modified: Tue, 18 Mar 2025 05:32:15 GMT  
		Size: 54.7 MB (54678888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e6ea165b50c90409bcc2021c84bb757614ecf3c10c11a0c866f97673091e36`  
		Last Modified: Tue, 18 Mar 2025 05:32:13 GMT  
		Size: 1.5 MB (1488212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12a2d23e63fd0ca0f9c767ac72fe75b2ff092e16511e166c978d9ad000246b9`  
		Last Modified: Tue, 18 Mar 2025 05:32:18 GMT  
		Size: 219.6 MB (219626045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7` - unknown; unknown

```console
$ docker pull dart@sha256:6f95762d375ba3eeae8aad857d442e2c220ee8fb9d163d2094effe5e2b5caaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d52c0a42000c08e48c92bca0cb052efe5fe4c425c94f38928e03a760d35c27a`

```dockerfile
```

-	Layers:
	-	`sha256:417cb0c8593799bfc188df240164693386c9ddfaa96d2ab8b1617c6bc857bed2`  
		Last Modified: Tue, 18 Mar 2025 05:32:13 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.7-sdk`

```console
$ docker pull dart@sha256:5e209253ec4b60200808157d99f3b1399aade3d449dbad537edcd95d54e50965
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.7-sdk` - linux; amd64

```console
$ docker pull dart@sha256:e7511450d0b8bbc00355012e911d058e982e8606a6c542b2b5d97b6b3a4e77ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305381719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0960803cd33ec18cf437a59477528d6a8ee32ae039f9692deb15657b0fe99eed`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Mar 2025 13:16:06 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 27 Mar 2025 13:16:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:16:06 GMT
WORKDIR /root
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679997ce086256ff83ecd067858ae7b3e78f0b23c25943535915494859cca1f8`  
		Last Modified: Tue, 08 Apr 2025 01:25:29 GMT  
		Size: 54.9 MB (54907945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a5f32ada0a0fcf930ede1717dd841fa3f5c6f64e8310bde9080529a41015b2`  
		Last Modified: Tue, 08 Apr 2025 01:25:28 GMT  
		Size: 1.8 MB (1785449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90f887541e2b4482dfd6c92ceb0527fc54d9b10614646e5da880ed99aee4dfb`  
		Last Modified: Tue, 08 Apr 2025 01:25:32 GMT  
		Size: 220.5 MB (220461034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a32403c56f9affea98af96da7f0ac7ba283edeb324ff741aab0f44eaf7cfddf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf4f1d80d172369e0d24cef022c6c0d9e83e60f43c022780c93c3df51692977`

```dockerfile
```

-	Layers:
	-	`sha256:404bb1ddc2df517b6fee1f7c088a9571d5fc6e5a84529591d775bbb8c7a357e5`  
		Last Modified: Tue, 08 Apr 2025 01:25:28 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d9c927c152b2c3d87e3ac69afd6328f9831a2875f33dcc4cc4cd425c40f735b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226291105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2261335dcf37c21db7f023a0451fa4ecdbc75b1fb9d59b127dd7f060398ea7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c93b8fd21f16e455ea78d5bde6caa154201a29de8b46231a24c2add8c4617b`  
		Last Modified: Tue, 18 Mar 2025 06:31:14 GMT  
		Size: 49.6 MB (49561746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3c3c9f9d55928fead9f3a4da4831bf52da646fa70eeb43ecaec385a9c4b68d`  
		Last Modified: Tue, 18 Mar 2025 06:31:12 GMT  
		Size: 1.2 MB (1221938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce883cc8a1d5b91b14d7dc7d44b8107de304cef7c3c386149cc8d1e279ea9eb3`  
		Last Modified: Tue, 18 Mar 2025 06:31:16 GMT  
		Size: 151.6 MB (151592301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e2eaee0b4542bba459542c17bf1b54bc120ed38a3ae9188f880c7d56b26231a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2823625c0f31d59bcaa795a19cff381dadba16d0b7dbb878c6c5a9a027e6543d`

```dockerfile
```

-	Layers:
	-	`sha256:7c42669dfe6ff893492a04fdddf54c8fa268ce6053f36c27b30a7c4fd129d247`  
		Last Modified: Tue, 18 Mar 2025 06:31:12 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:fa9072f808cb3c8ac1230498ac721ca055d5667a5e4e7c7f45dcd21a5bb8a5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303837214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b765cccbabb6cd73309fa9fd557e2e1ae8ac1eb7f7a0885e675c7c43b259a882`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0e44317139d437e3a0030b2a5681351b64688c925cabaf26c463eae756097d`  
		Last Modified: Tue, 18 Mar 2025 05:32:15 GMT  
		Size: 54.7 MB (54678888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e6ea165b50c90409bcc2021c84bb757614ecf3c10c11a0c866f97673091e36`  
		Last Modified: Tue, 18 Mar 2025 05:32:13 GMT  
		Size: 1.5 MB (1488212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12a2d23e63fd0ca0f9c767ac72fe75b2ff092e16511e166c978d9ad000246b9`  
		Last Modified: Tue, 18 Mar 2025 05:32:18 GMT  
		Size: 219.6 MB (219626045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6f95762d375ba3eeae8aad857d442e2c220ee8fb9d163d2094effe5e2b5caaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d52c0a42000c08e48c92bca0cb052efe5fe4c425c94f38928e03a760d35c27a`

```dockerfile
```

-	Layers:
	-	`sha256:417cb0c8593799bfc188df240164693386c9ddfaa96d2ab8b1617c6bc857bed2`  
		Last Modified: Tue, 18 Mar 2025 05:32:13 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.7.2`

```console
$ docker pull dart@sha256:5e209253ec4b60200808157d99f3b1399aade3d449dbad537edcd95d54e50965
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.7.2` - linux; amd64

```console
$ docker pull dart@sha256:e7511450d0b8bbc00355012e911d058e982e8606a6c542b2b5d97b6b3a4e77ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305381719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0960803cd33ec18cf437a59477528d6a8ee32ae039f9692deb15657b0fe99eed`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Mar 2025 13:16:06 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 27 Mar 2025 13:16:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:16:06 GMT
WORKDIR /root
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679997ce086256ff83ecd067858ae7b3e78f0b23c25943535915494859cca1f8`  
		Last Modified: Tue, 08 Apr 2025 01:25:29 GMT  
		Size: 54.9 MB (54907945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a5f32ada0a0fcf930ede1717dd841fa3f5c6f64e8310bde9080529a41015b2`  
		Last Modified: Tue, 08 Apr 2025 01:25:28 GMT  
		Size: 1.8 MB (1785449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90f887541e2b4482dfd6c92ceb0527fc54d9b10614646e5da880ed99aee4dfb`  
		Last Modified: Tue, 08 Apr 2025 01:25:32 GMT  
		Size: 220.5 MB (220461034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.2` - unknown; unknown

```console
$ docker pull dart@sha256:a32403c56f9affea98af96da7f0ac7ba283edeb324ff741aab0f44eaf7cfddf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf4f1d80d172369e0d24cef022c6c0d9e83e60f43c022780c93c3df51692977`

```dockerfile
```

-	Layers:
	-	`sha256:404bb1ddc2df517b6fee1f7c088a9571d5fc6e5a84529591d775bbb8c7a357e5`  
		Last Modified: Tue, 08 Apr 2025 01:25:28 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7.2` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d9c927c152b2c3d87e3ac69afd6328f9831a2875f33dcc4cc4cd425c40f735b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226291105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2261335dcf37c21db7f023a0451fa4ecdbc75b1fb9d59b127dd7f060398ea7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c93b8fd21f16e455ea78d5bde6caa154201a29de8b46231a24c2add8c4617b`  
		Last Modified: Tue, 18 Mar 2025 06:31:14 GMT  
		Size: 49.6 MB (49561746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3c3c9f9d55928fead9f3a4da4831bf52da646fa70eeb43ecaec385a9c4b68d`  
		Last Modified: Tue, 18 Mar 2025 06:31:12 GMT  
		Size: 1.2 MB (1221938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce883cc8a1d5b91b14d7dc7d44b8107de304cef7c3c386149cc8d1e279ea9eb3`  
		Last Modified: Tue, 18 Mar 2025 06:31:16 GMT  
		Size: 151.6 MB (151592301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.2` - unknown; unknown

```console
$ docker pull dart@sha256:e2eaee0b4542bba459542c17bf1b54bc120ed38a3ae9188f880c7d56b26231a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2823625c0f31d59bcaa795a19cff381dadba16d0b7dbb878c6c5a9a027e6543d`

```dockerfile
```

-	Layers:
	-	`sha256:7c42669dfe6ff893492a04fdddf54c8fa268ce6053f36c27b30a7c4fd129d247`  
		Last Modified: Tue, 18 Mar 2025 06:31:12 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7.2` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:fa9072f808cb3c8ac1230498ac721ca055d5667a5e4e7c7f45dcd21a5bb8a5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303837214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b765cccbabb6cd73309fa9fd557e2e1ae8ac1eb7f7a0885e675c7c43b259a882`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0e44317139d437e3a0030b2a5681351b64688c925cabaf26c463eae756097d`  
		Last Modified: Tue, 18 Mar 2025 05:32:15 GMT  
		Size: 54.7 MB (54678888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e6ea165b50c90409bcc2021c84bb757614ecf3c10c11a0c866f97673091e36`  
		Last Modified: Tue, 18 Mar 2025 05:32:13 GMT  
		Size: 1.5 MB (1488212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12a2d23e63fd0ca0f9c767ac72fe75b2ff092e16511e166c978d9ad000246b9`  
		Last Modified: Tue, 18 Mar 2025 05:32:18 GMT  
		Size: 219.6 MB (219626045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.2` - unknown; unknown

```console
$ docker pull dart@sha256:6f95762d375ba3eeae8aad857d442e2c220ee8fb9d163d2094effe5e2b5caaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d52c0a42000c08e48c92bca0cb052efe5fe4c425c94f38928e03a760d35c27a`

```dockerfile
```

-	Layers:
	-	`sha256:417cb0c8593799bfc188df240164693386c9ddfaa96d2ab8b1617c6bc857bed2`  
		Last Modified: Tue, 18 Mar 2025 05:32:13 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.7.2-sdk`

```console
$ docker pull dart@sha256:5e209253ec4b60200808157d99f3b1399aade3d449dbad537edcd95d54e50965
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.7.2-sdk` - linux; amd64

```console
$ docker pull dart@sha256:e7511450d0b8bbc00355012e911d058e982e8606a6c542b2b5d97b6b3a4e77ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305381719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0960803cd33ec18cf437a59477528d6a8ee32ae039f9692deb15657b0fe99eed`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Mar 2025 13:16:06 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 27 Mar 2025 13:16:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:16:06 GMT
WORKDIR /root
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679997ce086256ff83ecd067858ae7b3e78f0b23c25943535915494859cca1f8`  
		Last Modified: Tue, 08 Apr 2025 01:25:29 GMT  
		Size: 54.9 MB (54907945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a5f32ada0a0fcf930ede1717dd841fa3f5c6f64e8310bde9080529a41015b2`  
		Last Modified: Tue, 08 Apr 2025 01:25:28 GMT  
		Size: 1.8 MB (1785449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90f887541e2b4482dfd6c92ceb0527fc54d9b10614646e5da880ed99aee4dfb`  
		Last Modified: Tue, 08 Apr 2025 01:25:32 GMT  
		Size: 220.5 MB (220461034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.2-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a32403c56f9affea98af96da7f0ac7ba283edeb324ff741aab0f44eaf7cfddf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf4f1d80d172369e0d24cef022c6c0d9e83e60f43c022780c93c3df51692977`

```dockerfile
```

-	Layers:
	-	`sha256:404bb1ddc2df517b6fee1f7c088a9571d5fc6e5a84529591d775bbb8c7a357e5`  
		Last Modified: Tue, 08 Apr 2025 01:25:28 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7.2-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d9c927c152b2c3d87e3ac69afd6328f9831a2875f33dcc4cc4cd425c40f735b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226291105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2261335dcf37c21db7f023a0451fa4ecdbc75b1fb9d59b127dd7f060398ea7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c93b8fd21f16e455ea78d5bde6caa154201a29de8b46231a24c2add8c4617b`  
		Last Modified: Tue, 18 Mar 2025 06:31:14 GMT  
		Size: 49.6 MB (49561746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3c3c9f9d55928fead9f3a4da4831bf52da646fa70eeb43ecaec385a9c4b68d`  
		Last Modified: Tue, 18 Mar 2025 06:31:12 GMT  
		Size: 1.2 MB (1221938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce883cc8a1d5b91b14d7dc7d44b8107de304cef7c3c386149cc8d1e279ea9eb3`  
		Last Modified: Tue, 18 Mar 2025 06:31:16 GMT  
		Size: 151.6 MB (151592301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.2-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e2eaee0b4542bba459542c17bf1b54bc120ed38a3ae9188f880c7d56b26231a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2823625c0f31d59bcaa795a19cff381dadba16d0b7dbb878c6c5a9a027e6543d`

```dockerfile
```

-	Layers:
	-	`sha256:7c42669dfe6ff893492a04fdddf54c8fa268ce6053f36c27b30a7c4fd129d247`  
		Last Modified: Tue, 18 Mar 2025 06:31:12 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7.2-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:fa9072f808cb3c8ac1230498ac721ca055d5667a5e4e7c7f45dcd21a5bb8a5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303837214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b765cccbabb6cd73309fa9fd557e2e1ae8ac1eb7f7a0885e675c7c43b259a882`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0e44317139d437e3a0030b2a5681351b64688c925cabaf26c463eae756097d`  
		Last Modified: Tue, 18 Mar 2025 05:32:15 GMT  
		Size: 54.7 MB (54678888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e6ea165b50c90409bcc2021c84bb757614ecf3c10c11a0c866f97673091e36`  
		Last Modified: Tue, 18 Mar 2025 05:32:13 GMT  
		Size: 1.5 MB (1488212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12a2d23e63fd0ca0f9c767ac72fe75b2ff092e16511e166c978d9ad000246b9`  
		Last Modified: Tue, 18 Mar 2025 05:32:18 GMT  
		Size: 219.6 MB (219626045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.2-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6f95762d375ba3eeae8aad857d442e2c220ee8fb9d163d2094effe5e2b5caaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d52c0a42000c08e48c92bca0cb052efe5fe4c425c94f38928e03a760d35c27a`

```dockerfile
```

-	Layers:
	-	`sha256:417cb0c8593799bfc188df240164693386c9ddfaa96d2ab8b1617c6bc857bed2`  
		Last Modified: Tue, 18 Mar 2025 05:32:13 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8.0-171.2.beta`

```console
$ docker pull dart@sha256:11a2859dd4327fd95b99ebf966d7939797a6bbdbaefef2eb0285a68b54348f1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.8.0-171.2.beta` - linux; amd64

```console
$ docker pull dart@sha256:ef22f9dba7be94cd6717cec3cc19be2cde75dcc70e55c2955c6d84e5655dd496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 MB (297154468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf89b56f628ed829ede5bfb0f92d35f309fb1d07b8774a99b2315c52f6d7c69`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Mar 2025 13:16:06 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 27 Mar 2025 13:16:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:16:06 GMT
WORKDIR /root
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e7d9d48ac0a97a8265d338d71cabd16d53f87ecb96fcb1d8d327e89560cd09a0;             SDK_ARCH="x64";;         armhf)             DART_SHA256=90309132fee3ec78d790a443d00ff1a5d2bf7a7acf8c14b9ad3ef20c8da2cd38;             SDK_ARCH="arm";;         arm64)             DART_SHA256=23f2528c0ce40f5fc1720af97628a7dc78443d9012df4022b791972acb28646f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-171.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849635def0e85755541cf53d2434625118f7622bf6470cec17b2b0cc5cc0e9e5`  
		Last Modified: Tue, 08 Apr 2025 01:25:29 GMT  
		Size: 54.9 MB (54908048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff76ef7b2e334b35fbb0e5c333f92bc6b74cfcdb2dae32b0540e0a80091e9d3`  
		Last Modified: Tue, 08 Apr 2025 01:25:29 GMT  
		Size: 1.8 MB (1785449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a21783ca230d3b3fac7655ca61998b573e59bf10c667b7a6300a9ad9c010f2d`  
		Last Modified: Tue, 08 Apr 2025 01:25:32 GMT  
		Size: 212.2 MB (212233680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0-171.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:b8f8cac991b17df323177d9b1066a4f3b7ca5039af88d4511f04501cdbb97f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4398a1b9bf9654ad3d81010ee25bf1b3fdaf1ece285df547590a6f948924f84b`

```dockerfile
```

-	Layers:
	-	`sha256:892eb0e4898ab69ecd346355bb1c2fd3822af543e3a701c87f6fcf9622bfd476`  
		Last Modified: Tue, 08 Apr 2025 01:25:28 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.0-171.2.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:f6e6b0cd62538355aa4e482c1fe7acaa27b01fdebbae0a9298149f68277cb9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.2 MB (222219469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07900c814ea88e39eb23b77caf549d80645715e92b5b66b07f35ca8c5b4967c9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 27 Mar 2025 13:16:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:16:06 GMT
WORKDIR /root
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e7d9d48ac0a97a8265d338d71cabd16d53f87ecb96fcb1d8d327e89560cd09a0;             SDK_ARCH="x64";;         armhf)             DART_SHA256=90309132fee3ec78d790a443d00ff1a5d2bf7a7acf8c14b9ad3ef20c8da2cd38;             SDK_ARCH="arm";;         arm64)             DART_SHA256=23f2528c0ce40f5fc1720af97628a7dc78443d9012df4022b791972acb28646f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-171.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972839da75c60274dbfb6b7a02ff7ed1cb5db755f8e9b8242d787510a30fdc44`  
		Last Modified: Fri, 21 Mar 2025 16:29:59 GMT  
		Size: 49.6 MB (49562134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ce12a38521920d24bf7ce26f38e42745cfc4605890b8396fa5a739b9cacde5`  
		Last Modified: Fri, 21 Mar 2025 16:29:58 GMT  
		Size: 1.2 MB (1221939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1a79327b7db5fcf0a7251216c379fa889e65bf6249e4b129aefb437711ec4f`  
		Last Modified: Thu, 27 Mar 2025 19:00:29 GMT  
		Size: 147.5 MB (147520276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0-171.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:e8b52c086cda6967b8ea35cbf984019011d857729a993925fd106e8d0196748f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05c371ca5204e4d7951026fa87c4553f7eec562836590a6b19871018f549452`

```dockerfile
```

-	Layers:
	-	`sha256:8083439383838faf0cdbe432bbe4680f29a5695b02a73765fcf2fa84156228f2`  
		Last Modified: Thu, 27 Mar 2025 19:00:20 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.0-171.2.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4214a6003a4161130f2b34c8c458669fed08e32e9c7a86d525e4c734d6d8d1b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295684554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe92444c91ffb02f330032985dfd7d3cea7577f9e5aa52fd1b79780c350d420`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 27 Mar 2025 13:16:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:16:06 GMT
WORKDIR /root
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e7d9d48ac0a97a8265d338d71cabd16d53f87ecb96fcb1d8d327e89560cd09a0;             SDK_ARCH="x64";;         armhf)             DART_SHA256=90309132fee3ec78d790a443d00ff1a5d2bf7a7acf8c14b9ad3ef20c8da2cd38;             SDK_ARCH="arm";;         arm64)             DART_SHA256=23f2528c0ce40f5fc1720af97628a7dc78443d9012df4022b791972acb28646f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-171.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7e6f4deb8b735eb3fdb6f45dc31a56c1c1a0846c66a507925b08b830eb3a82`  
		Last Modified: Thu, 27 Mar 2025 19:00:48 GMT  
		Size: 54.7 MB (54678804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f62f6d165558e0c2bcba2afc4853cf33d244ec118b5307f95f51c61701627e`  
		Last Modified: Thu, 27 Mar 2025 19:00:46 GMT  
		Size: 1.5 MB (1488210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567bdf1f4d170c7ef8f10a746e5972b4f6334a4d0931e4cdbb491e995c3c4952`  
		Last Modified: Thu, 27 Mar 2025 19:00:51 GMT  
		Size: 211.5 MB (211473471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0-171.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:fee9f7670b00a76f2d28999400080d239e5c2ebc4c3ba7ab761968d4252cbe4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b502a88670ef93df934af1666e33b47b9a2ee766fb86ef53a44e15b85c25f5`

```dockerfile
```

-	Layers:
	-	`sha256:1c054c84d5f52958e48c7e77906684055327f73f9f51ca71f8ec220e8a4dd246`  
		Last Modified: Thu, 27 Mar 2025 19:00:46 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8.0-171.2.beta-sdk`

```console
$ docker pull dart@sha256:11a2859dd4327fd95b99ebf966d7939797a6bbdbaefef2eb0285a68b54348f1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.8.0-171.2.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:ef22f9dba7be94cd6717cec3cc19be2cde75dcc70e55c2955c6d84e5655dd496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 MB (297154468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf89b56f628ed829ede5bfb0f92d35f309fb1d07b8774a99b2315c52f6d7c69`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Mar 2025 13:16:06 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 27 Mar 2025 13:16:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:16:06 GMT
WORKDIR /root
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e7d9d48ac0a97a8265d338d71cabd16d53f87ecb96fcb1d8d327e89560cd09a0;             SDK_ARCH="x64";;         armhf)             DART_SHA256=90309132fee3ec78d790a443d00ff1a5d2bf7a7acf8c14b9ad3ef20c8da2cd38;             SDK_ARCH="arm";;         arm64)             DART_SHA256=23f2528c0ce40f5fc1720af97628a7dc78443d9012df4022b791972acb28646f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-171.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849635def0e85755541cf53d2434625118f7622bf6470cec17b2b0cc5cc0e9e5`  
		Last Modified: Tue, 08 Apr 2025 01:25:29 GMT  
		Size: 54.9 MB (54908048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff76ef7b2e334b35fbb0e5c333f92bc6b74cfcdb2dae32b0540e0a80091e9d3`  
		Last Modified: Tue, 08 Apr 2025 01:25:29 GMT  
		Size: 1.8 MB (1785449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a21783ca230d3b3fac7655ca61998b573e59bf10c667b7a6300a9ad9c010f2d`  
		Last Modified: Tue, 08 Apr 2025 01:25:32 GMT  
		Size: 212.2 MB (212233680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0-171.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b8f8cac991b17df323177d9b1066a4f3b7ca5039af88d4511f04501cdbb97f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4398a1b9bf9654ad3d81010ee25bf1b3fdaf1ece285df547590a6f948924f84b`

```dockerfile
```

-	Layers:
	-	`sha256:892eb0e4898ab69ecd346355bb1c2fd3822af543e3a701c87f6fcf9622bfd476`  
		Last Modified: Tue, 08 Apr 2025 01:25:28 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.0-171.2.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:f6e6b0cd62538355aa4e482c1fe7acaa27b01fdebbae0a9298149f68277cb9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.2 MB (222219469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07900c814ea88e39eb23b77caf549d80645715e92b5b66b07f35ca8c5b4967c9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 27 Mar 2025 13:16:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:16:06 GMT
WORKDIR /root
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e7d9d48ac0a97a8265d338d71cabd16d53f87ecb96fcb1d8d327e89560cd09a0;             SDK_ARCH="x64";;         armhf)             DART_SHA256=90309132fee3ec78d790a443d00ff1a5d2bf7a7acf8c14b9ad3ef20c8da2cd38;             SDK_ARCH="arm";;         arm64)             DART_SHA256=23f2528c0ce40f5fc1720af97628a7dc78443d9012df4022b791972acb28646f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-171.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972839da75c60274dbfb6b7a02ff7ed1cb5db755f8e9b8242d787510a30fdc44`  
		Last Modified: Fri, 21 Mar 2025 16:29:59 GMT  
		Size: 49.6 MB (49562134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ce12a38521920d24bf7ce26f38e42745cfc4605890b8396fa5a739b9cacde5`  
		Last Modified: Fri, 21 Mar 2025 16:29:58 GMT  
		Size: 1.2 MB (1221939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1a79327b7db5fcf0a7251216c379fa889e65bf6249e4b129aefb437711ec4f`  
		Last Modified: Thu, 27 Mar 2025 19:00:29 GMT  
		Size: 147.5 MB (147520276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0-171.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e8b52c086cda6967b8ea35cbf984019011d857729a993925fd106e8d0196748f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05c371ca5204e4d7951026fa87c4553f7eec562836590a6b19871018f549452`

```dockerfile
```

-	Layers:
	-	`sha256:8083439383838faf0cdbe432bbe4680f29a5695b02a73765fcf2fa84156228f2`  
		Last Modified: Thu, 27 Mar 2025 19:00:20 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.0-171.2.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4214a6003a4161130f2b34c8c458669fed08e32e9c7a86d525e4c734d6d8d1b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295684554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe92444c91ffb02f330032985dfd7d3cea7577f9e5aa52fd1b79780c350d420`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 27 Mar 2025 13:16:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:16:06 GMT
WORKDIR /root
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e7d9d48ac0a97a8265d338d71cabd16d53f87ecb96fcb1d8d327e89560cd09a0;             SDK_ARCH="x64";;         armhf)             DART_SHA256=90309132fee3ec78d790a443d00ff1a5d2bf7a7acf8c14b9ad3ef20c8da2cd38;             SDK_ARCH="arm";;         arm64)             DART_SHA256=23f2528c0ce40f5fc1720af97628a7dc78443d9012df4022b791972acb28646f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-171.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7e6f4deb8b735eb3fdb6f45dc31a56c1c1a0846c66a507925b08b830eb3a82`  
		Last Modified: Thu, 27 Mar 2025 19:00:48 GMT  
		Size: 54.7 MB (54678804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f62f6d165558e0c2bcba2afc4853cf33d244ec118b5307f95f51c61701627e`  
		Last Modified: Thu, 27 Mar 2025 19:00:46 GMT  
		Size: 1.5 MB (1488210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567bdf1f4d170c7ef8f10a746e5972b4f6334a4d0931e4cdbb491e995c3c4952`  
		Last Modified: Thu, 27 Mar 2025 19:00:51 GMT  
		Size: 211.5 MB (211473471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0-171.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:fee9f7670b00a76f2d28999400080d239e5c2ebc4c3ba7ab761968d4252cbe4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b502a88670ef93df934af1666e33b47b9a2ee766fb86ef53a44e15b85c25f5`

```dockerfile
```

-	Layers:
	-	`sha256:1c054c84d5f52958e48c7e77906684055327f73f9f51ca71f8ec220e8a4dd246`  
		Last Modified: Thu, 27 Mar 2025 19:00:46 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:11a2859dd4327fd95b99ebf966d7939797a6bbdbaefef2eb0285a68b54348f1e
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
$ docker pull dart@sha256:ef22f9dba7be94cd6717cec3cc19be2cde75dcc70e55c2955c6d84e5655dd496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 MB (297154468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf89b56f628ed829ede5bfb0f92d35f309fb1d07b8774a99b2315c52f6d7c69`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Mar 2025 13:16:06 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 27 Mar 2025 13:16:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:16:06 GMT
WORKDIR /root
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e7d9d48ac0a97a8265d338d71cabd16d53f87ecb96fcb1d8d327e89560cd09a0;             SDK_ARCH="x64";;         armhf)             DART_SHA256=90309132fee3ec78d790a443d00ff1a5d2bf7a7acf8c14b9ad3ef20c8da2cd38;             SDK_ARCH="arm";;         arm64)             DART_SHA256=23f2528c0ce40f5fc1720af97628a7dc78443d9012df4022b791972acb28646f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-171.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849635def0e85755541cf53d2434625118f7622bf6470cec17b2b0cc5cc0e9e5`  
		Last Modified: Tue, 08 Apr 2025 01:25:29 GMT  
		Size: 54.9 MB (54908048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff76ef7b2e334b35fbb0e5c333f92bc6b74cfcdb2dae32b0540e0a80091e9d3`  
		Last Modified: Tue, 08 Apr 2025 01:25:29 GMT  
		Size: 1.8 MB (1785449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a21783ca230d3b3fac7655ca61998b573e59bf10c667b7a6300a9ad9c010f2d`  
		Last Modified: Tue, 08 Apr 2025 01:25:32 GMT  
		Size: 212.2 MB (212233680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:b8f8cac991b17df323177d9b1066a4f3b7ca5039af88d4511f04501cdbb97f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4398a1b9bf9654ad3d81010ee25bf1b3fdaf1ece285df547590a6f948924f84b`

```dockerfile
```

-	Layers:
	-	`sha256:892eb0e4898ab69ecd346355bb1c2fd3822af543e3a701c87f6fcf9622bfd476`  
		Last Modified: Tue, 08 Apr 2025 01:25:28 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:f6e6b0cd62538355aa4e482c1fe7acaa27b01fdebbae0a9298149f68277cb9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.2 MB (222219469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07900c814ea88e39eb23b77caf549d80645715e92b5b66b07f35ca8c5b4967c9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 27 Mar 2025 13:16:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:16:06 GMT
WORKDIR /root
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e7d9d48ac0a97a8265d338d71cabd16d53f87ecb96fcb1d8d327e89560cd09a0;             SDK_ARCH="x64";;         armhf)             DART_SHA256=90309132fee3ec78d790a443d00ff1a5d2bf7a7acf8c14b9ad3ef20c8da2cd38;             SDK_ARCH="arm";;         arm64)             DART_SHA256=23f2528c0ce40f5fc1720af97628a7dc78443d9012df4022b791972acb28646f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-171.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972839da75c60274dbfb6b7a02ff7ed1cb5db755f8e9b8242d787510a30fdc44`  
		Last Modified: Fri, 21 Mar 2025 16:29:59 GMT  
		Size: 49.6 MB (49562134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ce12a38521920d24bf7ce26f38e42745cfc4605890b8396fa5a739b9cacde5`  
		Last Modified: Fri, 21 Mar 2025 16:29:58 GMT  
		Size: 1.2 MB (1221939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1a79327b7db5fcf0a7251216c379fa889e65bf6249e4b129aefb437711ec4f`  
		Last Modified: Thu, 27 Mar 2025 19:00:29 GMT  
		Size: 147.5 MB (147520276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:e8b52c086cda6967b8ea35cbf984019011d857729a993925fd106e8d0196748f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05c371ca5204e4d7951026fa87c4553f7eec562836590a6b19871018f549452`

```dockerfile
```

-	Layers:
	-	`sha256:8083439383838faf0cdbe432bbe4680f29a5695b02a73765fcf2fa84156228f2`  
		Last Modified: Thu, 27 Mar 2025 19:00:20 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4214a6003a4161130f2b34c8c458669fed08e32e9c7a86d525e4c734d6d8d1b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295684554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe92444c91ffb02f330032985dfd7d3cea7577f9e5aa52fd1b79780c350d420`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 27 Mar 2025 13:16:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:16:06 GMT
WORKDIR /root
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e7d9d48ac0a97a8265d338d71cabd16d53f87ecb96fcb1d8d327e89560cd09a0;             SDK_ARCH="x64";;         armhf)             DART_SHA256=90309132fee3ec78d790a443d00ff1a5d2bf7a7acf8c14b9ad3ef20c8da2cd38;             SDK_ARCH="arm";;         arm64)             DART_SHA256=23f2528c0ce40f5fc1720af97628a7dc78443d9012df4022b791972acb28646f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-171.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7e6f4deb8b735eb3fdb6f45dc31a56c1c1a0846c66a507925b08b830eb3a82`  
		Last Modified: Thu, 27 Mar 2025 19:00:48 GMT  
		Size: 54.7 MB (54678804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f62f6d165558e0c2bcba2afc4853cf33d244ec118b5307f95f51c61701627e`  
		Last Modified: Thu, 27 Mar 2025 19:00:46 GMT  
		Size: 1.5 MB (1488210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567bdf1f4d170c7ef8f10a746e5972b4f6334a4d0931e4cdbb491e995c3c4952`  
		Last Modified: Thu, 27 Mar 2025 19:00:51 GMT  
		Size: 211.5 MB (211473471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:fee9f7670b00a76f2d28999400080d239e5c2ebc4c3ba7ab761968d4252cbe4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b502a88670ef93df934af1666e33b47b9a2ee766fb86ef53a44e15b85c25f5`

```dockerfile
```

-	Layers:
	-	`sha256:1c054c84d5f52958e48c7e77906684055327f73f9f51ca71f8ec220e8a4dd246`  
		Last Modified: Thu, 27 Mar 2025 19:00:46 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:11a2859dd4327fd95b99ebf966d7939797a6bbdbaefef2eb0285a68b54348f1e
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
$ docker pull dart@sha256:ef22f9dba7be94cd6717cec3cc19be2cde75dcc70e55c2955c6d84e5655dd496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 MB (297154468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf89b56f628ed829ede5bfb0f92d35f309fb1d07b8774a99b2315c52f6d7c69`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Mar 2025 13:16:06 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 27 Mar 2025 13:16:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:16:06 GMT
WORKDIR /root
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e7d9d48ac0a97a8265d338d71cabd16d53f87ecb96fcb1d8d327e89560cd09a0;             SDK_ARCH="x64";;         armhf)             DART_SHA256=90309132fee3ec78d790a443d00ff1a5d2bf7a7acf8c14b9ad3ef20c8da2cd38;             SDK_ARCH="arm";;         arm64)             DART_SHA256=23f2528c0ce40f5fc1720af97628a7dc78443d9012df4022b791972acb28646f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-171.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849635def0e85755541cf53d2434625118f7622bf6470cec17b2b0cc5cc0e9e5`  
		Last Modified: Tue, 08 Apr 2025 01:25:29 GMT  
		Size: 54.9 MB (54908048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff76ef7b2e334b35fbb0e5c333f92bc6b74cfcdb2dae32b0540e0a80091e9d3`  
		Last Modified: Tue, 08 Apr 2025 01:25:29 GMT  
		Size: 1.8 MB (1785449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a21783ca230d3b3fac7655ca61998b573e59bf10c667b7a6300a9ad9c010f2d`  
		Last Modified: Tue, 08 Apr 2025 01:25:32 GMT  
		Size: 212.2 MB (212233680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b8f8cac991b17df323177d9b1066a4f3b7ca5039af88d4511f04501cdbb97f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4398a1b9bf9654ad3d81010ee25bf1b3fdaf1ece285df547590a6f948924f84b`

```dockerfile
```

-	Layers:
	-	`sha256:892eb0e4898ab69ecd346355bb1c2fd3822af543e3a701c87f6fcf9622bfd476`  
		Last Modified: Tue, 08 Apr 2025 01:25:28 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:f6e6b0cd62538355aa4e482c1fe7acaa27b01fdebbae0a9298149f68277cb9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.2 MB (222219469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07900c814ea88e39eb23b77caf549d80645715e92b5b66b07f35ca8c5b4967c9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 27 Mar 2025 13:16:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:16:06 GMT
WORKDIR /root
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e7d9d48ac0a97a8265d338d71cabd16d53f87ecb96fcb1d8d327e89560cd09a0;             SDK_ARCH="x64";;         armhf)             DART_SHA256=90309132fee3ec78d790a443d00ff1a5d2bf7a7acf8c14b9ad3ef20c8da2cd38;             SDK_ARCH="arm";;         arm64)             DART_SHA256=23f2528c0ce40f5fc1720af97628a7dc78443d9012df4022b791972acb28646f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-171.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972839da75c60274dbfb6b7a02ff7ed1cb5db755f8e9b8242d787510a30fdc44`  
		Last Modified: Fri, 21 Mar 2025 16:29:59 GMT  
		Size: 49.6 MB (49562134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ce12a38521920d24bf7ce26f38e42745cfc4605890b8396fa5a739b9cacde5`  
		Last Modified: Fri, 21 Mar 2025 16:29:58 GMT  
		Size: 1.2 MB (1221939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1a79327b7db5fcf0a7251216c379fa889e65bf6249e4b129aefb437711ec4f`  
		Last Modified: Thu, 27 Mar 2025 19:00:29 GMT  
		Size: 147.5 MB (147520276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e8b52c086cda6967b8ea35cbf984019011d857729a993925fd106e8d0196748f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05c371ca5204e4d7951026fa87c4553f7eec562836590a6b19871018f549452`

```dockerfile
```

-	Layers:
	-	`sha256:8083439383838faf0cdbe432bbe4680f29a5695b02a73765fcf2fa84156228f2`  
		Last Modified: Thu, 27 Mar 2025 19:00:20 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4214a6003a4161130f2b34c8c458669fed08e32e9c7a86d525e4c734d6d8d1b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295684554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe92444c91ffb02f330032985dfd7d3cea7577f9e5aa52fd1b79780c350d420`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 27 Mar 2025 13:16:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:16:06 GMT
WORKDIR /root
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e7d9d48ac0a97a8265d338d71cabd16d53f87ecb96fcb1d8d327e89560cd09a0;             SDK_ARCH="x64";;         armhf)             DART_SHA256=90309132fee3ec78d790a443d00ff1a5d2bf7a7acf8c14b9ad3ef20c8da2cd38;             SDK_ARCH="arm";;         arm64)             DART_SHA256=23f2528c0ce40f5fc1720af97628a7dc78443d9012df4022b791972acb28646f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-171.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7e6f4deb8b735eb3fdb6f45dc31a56c1c1a0846c66a507925b08b830eb3a82`  
		Last Modified: Thu, 27 Mar 2025 19:00:48 GMT  
		Size: 54.7 MB (54678804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f62f6d165558e0c2bcba2afc4853cf33d244ec118b5307f95f51c61701627e`  
		Last Modified: Thu, 27 Mar 2025 19:00:46 GMT  
		Size: 1.5 MB (1488210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567bdf1f4d170c7ef8f10a746e5972b4f6334a4d0931e4cdbb491e995c3c4952`  
		Last Modified: Thu, 27 Mar 2025 19:00:51 GMT  
		Size: 211.5 MB (211473471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:fee9f7670b00a76f2d28999400080d239e5c2ebc4c3ba7ab761968d4252cbe4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b502a88670ef93df934af1666e33b47b9a2ee766fb86ef53a44e15b85c25f5`

```dockerfile
```

-	Layers:
	-	`sha256:1c054c84d5f52958e48c7e77906684055327f73f9f51ca71f8ec220e8a4dd246`  
		Last Modified: Thu, 27 Mar 2025 19:00:46 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:5e209253ec4b60200808157d99f3b1399aade3d449dbad537edcd95d54e50965
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
$ docker pull dart@sha256:e7511450d0b8bbc00355012e911d058e982e8606a6c542b2b5d97b6b3a4e77ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305381719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0960803cd33ec18cf437a59477528d6a8ee32ae039f9692deb15657b0fe99eed`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Mar 2025 13:16:06 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 27 Mar 2025 13:16:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:16:06 GMT
WORKDIR /root
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679997ce086256ff83ecd067858ae7b3e78f0b23c25943535915494859cca1f8`  
		Last Modified: Tue, 08 Apr 2025 01:25:29 GMT  
		Size: 54.9 MB (54907945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a5f32ada0a0fcf930ede1717dd841fa3f5c6f64e8310bde9080529a41015b2`  
		Last Modified: Tue, 08 Apr 2025 01:25:28 GMT  
		Size: 1.8 MB (1785449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90f887541e2b4482dfd6c92ceb0527fc54d9b10614646e5da880ed99aee4dfb`  
		Last Modified: Tue, 08 Apr 2025 01:25:32 GMT  
		Size: 220.5 MB (220461034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:a32403c56f9affea98af96da7f0ac7ba283edeb324ff741aab0f44eaf7cfddf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf4f1d80d172369e0d24cef022c6c0d9e83e60f43c022780c93c3df51692977`

```dockerfile
```

-	Layers:
	-	`sha256:404bb1ddc2df517b6fee1f7c088a9571d5fc6e5a84529591d775bbb8c7a357e5`  
		Last Modified: Tue, 08 Apr 2025 01:25:28 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d9c927c152b2c3d87e3ac69afd6328f9831a2875f33dcc4cc4cd425c40f735b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226291105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2261335dcf37c21db7f023a0451fa4ecdbc75b1fb9d59b127dd7f060398ea7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c93b8fd21f16e455ea78d5bde6caa154201a29de8b46231a24c2add8c4617b`  
		Last Modified: Tue, 18 Mar 2025 06:31:14 GMT  
		Size: 49.6 MB (49561746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3c3c9f9d55928fead9f3a4da4831bf52da646fa70eeb43ecaec385a9c4b68d`  
		Last Modified: Tue, 18 Mar 2025 06:31:12 GMT  
		Size: 1.2 MB (1221938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce883cc8a1d5b91b14d7dc7d44b8107de304cef7c3c386149cc8d1e279ea9eb3`  
		Last Modified: Tue, 18 Mar 2025 06:31:16 GMT  
		Size: 151.6 MB (151592301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:e2eaee0b4542bba459542c17bf1b54bc120ed38a3ae9188f880c7d56b26231a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2823625c0f31d59bcaa795a19cff381dadba16d0b7dbb878c6c5a9a027e6543d`

```dockerfile
```

-	Layers:
	-	`sha256:7c42669dfe6ff893492a04fdddf54c8fa268ce6053f36c27b30a7c4fd129d247`  
		Last Modified: Tue, 18 Mar 2025 06:31:12 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:fa9072f808cb3c8ac1230498ac721ca055d5667a5e4e7c7f45dcd21a5bb8a5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303837214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b765cccbabb6cd73309fa9fd557e2e1ae8ac1eb7f7a0885e675c7c43b259a882`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0e44317139d437e3a0030b2a5681351b64688c925cabaf26c463eae756097d`  
		Last Modified: Tue, 18 Mar 2025 05:32:15 GMT  
		Size: 54.7 MB (54678888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e6ea165b50c90409bcc2021c84bb757614ecf3c10c11a0c866f97673091e36`  
		Last Modified: Tue, 18 Mar 2025 05:32:13 GMT  
		Size: 1.5 MB (1488212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12a2d23e63fd0ca0f9c767ac72fe75b2ff092e16511e166c978d9ad000246b9`  
		Last Modified: Tue, 18 Mar 2025 05:32:18 GMT  
		Size: 219.6 MB (219626045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:6f95762d375ba3eeae8aad857d442e2c220ee8fb9d163d2094effe5e2b5caaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d52c0a42000c08e48c92bca0cb052efe5fe4c425c94f38928e03a760d35c27a`

```dockerfile
```

-	Layers:
	-	`sha256:417cb0c8593799bfc188df240164693386c9ddfaa96d2ab8b1617c6bc857bed2`  
		Last Modified: Tue, 18 Mar 2025 05:32:13 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:5e209253ec4b60200808157d99f3b1399aade3d449dbad537edcd95d54e50965
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
$ docker pull dart@sha256:e7511450d0b8bbc00355012e911d058e982e8606a6c542b2b5d97b6b3a4e77ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305381719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0960803cd33ec18cf437a59477528d6a8ee32ae039f9692deb15657b0fe99eed`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Mar 2025 13:16:06 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 27 Mar 2025 13:16:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:16:06 GMT
WORKDIR /root
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679997ce086256ff83ecd067858ae7b3e78f0b23c25943535915494859cca1f8`  
		Last Modified: Tue, 08 Apr 2025 01:25:29 GMT  
		Size: 54.9 MB (54907945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a5f32ada0a0fcf930ede1717dd841fa3f5c6f64e8310bde9080529a41015b2`  
		Last Modified: Tue, 08 Apr 2025 01:25:28 GMT  
		Size: 1.8 MB (1785449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90f887541e2b4482dfd6c92ceb0527fc54d9b10614646e5da880ed99aee4dfb`  
		Last Modified: Tue, 08 Apr 2025 01:25:32 GMT  
		Size: 220.5 MB (220461034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a32403c56f9affea98af96da7f0ac7ba283edeb324ff741aab0f44eaf7cfddf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf4f1d80d172369e0d24cef022c6c0d9e83e60f43c022780c93c3df51692977`

```dockerfile
```

-	Layers:
	-	`sha256:404bb1ddc2df517b6fee1f7c088a9571d5fc6e5a84529591d775bbb8c7a357e5`  
		Last Modified: Tue, 08 Apr 2025 01:25:28 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d9c927c152b2c3d87e3ac69afd6328f9831a2875f33dcc4cc4cd425c40f735b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226291105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2261335dcf37c21db7f023a0451fa4ecdbc75b1fb9d59b127dd7f060398ea7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c93b8fd21f16e455ea78d5bde6caa154201a29de8b46231a24c2add8c4617b`  
		Last Modified: Tue, 18 Mar 2025 06:31:14 GMT  
		Size: 49.6 MB (49561746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3c3c9f9d55928fead9f3a4da4831bf52da646fa70eeb43ecaec385a9c4b68d`  
		Last Modified: Tue, 18 Mar 2025 06:31:12 GMT  
		Size: 1.2 MB (1221938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce883cc8a1d5b91b14d7dc7d44b8107de304cef7c3c386149cc8d1e279ea9eb3`  
		Last Modified: Tue, 18 Mar 2025 06:31:16 GMT  
		Size: 151.6 MB (151592301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e2eaee0b4542bba459542c17bf1b54bc120ed38a3ae9188f880c7d56b26231a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2823625c0f31d59bcaa795a19cff381dadba16d0b7dbb878c6c5a9a027e6543d`

```dockerfile
```

-	Layers:
	-	`sha256:7c42669dfe6ff893492a04fdddf54c8fa268ce6053f36c27b30a7c4fd129d247`  
		Last Modified: Tue, 18 Mar 2025 06:31:12 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:fa9072f808cb3c8ac1230498ac721ca055d5667a5e4e7c7f45dcd21a5bb8a5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303837214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b765cccbabb6cd73309fa9fd557e2e1ae8ac1eb7f7a0885e675c7c43b259a882`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0e44317139d437e3a0030b2a5681351b64688c925cabaf26c463eae756097d`  
		Last Modified: Tue, 18 Mar 2025 05:32:15 GMT  
		Size: 54.7 MB (54678888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e6ea165b50c90409bcc2021c84bb757614ecf3c10c11a0c866f97673091e36`  
		Last Modified: Tue, 18 Mar 2025 05:32:13 GMT  
		Size: 1.5 MB (1488212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12a2d23e63fd0ca0f9c767ac72fe75b2ff092e16511e166c978d9ad000246b9`  
		Last Modified: Tue, 18 Mar 2025 05:32:18 GMT  
		Size: 219.6 MB (219626045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6f95762d375ba3eeae8aad857d442e2c220ee8fb9d163d2094effe5e2b5caaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d52c0a42000c08e48c92bca0cb052efe5fe4c425c94f38928e03a760d35c27a`

```dockerfile
```

-	Layers:
	-	`sha256:417cb0c8593799bfc188df240164693386c9ddfaa96d2ab8b1617c6bc857bed2`  
		Last Modified: Tue, 18 Mar 2025 05:32:13 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:5e209253ec4b60200808157d99f3b1399aade3d449dbad537edcd95d54e50965
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
$ docker pull dart@sha256:e7511450d0b8bbc00355012e911d058e982e8606a6c542b2b5d97b6b3a4e77ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305381719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0960803cd33ec18cf437a59477528d6a8ee32ae039f9692deb15657b0fe99eed`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Mar 2025 13:16:06 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 27 Mar 2025 13:16:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:16:06 GMT
WORKDIR /root
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679997ce086256ff83ecd067858ae7b3e78f0b23c25943535915494859cca1f8`  
		Last Modified: Tue, 08 Apr 2025 01:25:29 GMT  
		Size: 54.9 MB (54907945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a5f32ada0a0fcf930ede1717dd841fa3f5c6f64e8310bde9080529a41015b2`  
		Last Modified: Tue, 08 Apr 2025 01:25:28 GMT  
		Size: 1.8 MB (1785449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90f887541e2b4482dfd6c92ceb0527fc54d9b10614646e5da880ed99aee4dfb`  
		Last Modified: Tue, 08 Apr 2025 01:25:32 GMT  
		Size: 220.5 MB (220461034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:a32403c56f9affea98af96da7f0ac7ba283edeb324ff741aab0f44eaf7cfddf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf4f1d80d172369e0d24cef022c6c0d9e83e60f43c022780c93c3df51692977`

```dockerfile
```

-	Layers:
	-	`sha256:404bb1ddc2df517b6fee1f7c088a9571d5fc6e5a84529591d775bbb8c7a357e5`  
		Last Modified: Tue, 08 Apr 2025 01:25:28 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d9c927c152b2c3d87e3ac69afd6328f9831a2875f33dcc4cc4cd425c40f735b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226291105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2261335dcf37c21db7f023a0451fa4ecdbc75b1fb9d59b127dd7f060398ea7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c93b8fd21f16e455ea78d5bde6caa154201a29de8b46231a24c2add8c4617b`  
		Last Modified: Tue, 18 Mar 2025 06:31:14 GMT  
		Size: 49.6 MB (49561746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3c3c9f9d55928fead9f3a4da4831bf52da646fa70eeb43ecaec385a9c4b68d`  
		Last Modified: Tue, 18 Mar 2025 06:31:12 GMT  
		Size: 1.2 MB (1221938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce883cc8a1d5b91b14d7dc7d44b8107de304cef7c3c386149cc8d1e279ea9eb3`  
		Last Modified: Tue, 18 Mar 2025 06:31:16 GMT  
		Size: 151.6 MB (151592301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:e2eaee0b4542bba459542c17bf1b54bc120ed38a3ae9188f880c7d56b26231a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2823625c0f31d59bcaa795a19cff381dadba16d0b7dbb878c6c5a9a027e6543d`

```dockerfile
```

-	Layers:
	-	`sha256:7c42669dfe6ff893492a04fdddf54c8fa268ce6053f36c27b30a7c4fd129d247`  
		Last Modified: Tue, 18 Mar 2025 06:31:12 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:fa9072f808cb3c8ac1230498ac721ca055d5667a5e4e7c7f45dcd21a5bb8a5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303837214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b765cccbabb6cd73309fa9fd557e2e1ae8ac1eb7f7a0885e675c7c43b259a882`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0e44317139d437e3a0030b2a5681351b64688c925cabaf26c463eae756097d`  
		Last Modified: Tue, 18 Mar 2025 05:32:15 GMT  
		Size: 54.7 MB (54678888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e6ea165b50c90409bcc2021c84bb757614ecf3c10c11a0c866f97673091e36`  
		Last Modified: Tue, 18 Mar 2025 05:32:13 GMT  
		Size: 1.5 MB (1488212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12a2d23e63fd0ca0f9c767ac72fe75b2ff092e16511e166c978d9ad000246b9`  
		Last Modified: Tue, 18 Mar 2025 05:32:18 GMT  
		Size: 219.6 MB (219626045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:6f95762d375ba3eeae8aad857d442e2c220ee8fb9d163d2094effe5e2b5caaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d52c0a42000c08e48c92bca0cb052efe5fe4c425c94f38928e03a760d35c27a`

```dockerfile
```

-	Layers:
	-	`sha256:417cb0c8593799bfc188df240164693386c9ddfaa96d2ab8b1617c6bc857bed2`  
		Last Modified: Tue, 18 Mar 2025 05:32:13 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:5e209253ec4b60200808157d99f3b1399aade3d449dbad537edcd95d54e50965
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
$ docker pull dart@sha256:e7511450d0b8bbc00355012e911d058e982e8606a6c542b2b5d97b6b3a4e77ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305381719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0960803cd33ec18cf437a59477528d6a8ee32ae039f9692deb15657b0fe99eed`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Mar 2025 13:16:06 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 27 Mar 2025 13:16:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 27 Mar 2025 13:16:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:16:06 GMT
WORKDIR /root
# Thu, 27 Mar 2025 13:16:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679997ce086256ff83ecd067858ae7b3e78f0b23c25943535915494859cca1f8`  
		Last Modified: Tue, 08 Apr 2025 01:25:29 GMT  
		Size: 54.9 MB (54907945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a5f32ada0a0fcf930ede1717dd841fa3f5c6f64e8310bde9080529a41015b2`  
		Last Modified: Tue, 08 Apr 2025 01:25:28 GMT  
		Size: 1.8 MB (1785449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90f887541e2b4482dfd6c92ceb0527fc54d9b10614646e5da880ed99aee4dfb`  
		Last Modified: Tue, 08 Apr 2025 01:25:32 GMT  
		Size: 220.5 MB (220461034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a32403c56f9affea98af96da7f0ac7ba283edeb324ff741aab0f44eaf7cfddf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf4f1d80d172369e0d24cef022c6c0d9e83e60f43c022780c93c3df51692977`

```dockerfile
```

-	Layers:
	-	`sha256:404bb1ddc2df517b6fee1f7c088a9571d5fc6e5a84529591d775bbb8c7a357e5`  
		Last Modified: Tue, 08 Apr 2025 01:25:28 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d9c927c152b2c3d87e3ac69afd6328f9831a2875f33dcc4cc4cd425c40f735b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226291105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2261335dcf37c21db7f023a0451fa4ecdbc75b1fb9d59b127dd7f060398ea7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c93b8fd21f16e455ea78d5bde6caa154201a29de8b46231a24c2add8c4617b`  
		Last Modified: Tue, 18 Mar 2025 06:31:14 GMT  
		Size: 49.6 MB (49561746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3c3c9f9d55928fead9f3a4da4831bf52da646fa70eeb43ecaec385a9c4b68d`  
		Last Modified: Tue, 18 Mar 2025 06:31:12 GMT  
		Size: 1.2 MB (1221938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce883cc8a1d5b91b14d7dc7d44b8107de304cef7c3c386149cc8d1e279ea9eb3`  
		Last Modified: Tue, 18 Mar 2025 06:31:16 GMT  
		Size: 151.6 MB (151592301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e2eaee0b4542bba459542c17bf1b54bc120ed38a3ae9188f880c7d56b26231a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2823625c0f31d59bcaa795a19cff381dadba16d0b7dbb878c6c5a9a027e6543d`

```dockerfile
```

-	Layers:
	-	`sha256:7c42669dfe6ff893492a04fdddf54c8fa268ce6053f36c27b30a7c4fd129d247`  
		Last Modified: Tue, 18 Mar 2025 06:31:12 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:fa9072f808cb3c8ac1230498ac721ca055d5667a5e4e7c7f45dcd21a5bb8a5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303837214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b765cccbabb6cd73309fa9fd557e2e1ae8ac1eb7f7a0885e675c7c43b259a882`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0e44317139d437e3a0030b2a5681351b64688c925cabaf26c463eae756097d`  
		Last Modified: Tue, 18 Mar 2025 05:32:15 GMT  
		Size: 54.7 MB (54678888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e6ea165b50c90409bcc2021c84bb757614ecf3c10c11a0c866f97673091e36`  
		Last Modified: Tue, 18 Mar 2025 05:32:13 GMT  
		Size: 1.5 MB (1488212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12a2d23e63fd0ca0f9c767ac72fe75b2ff092e16511e166c978d9ad000246b9`  
		Last Modified: Tue, 18 Mar 2025 05:32:18 GMT  
		Size: 219.6 MB (219626045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6f95762d375ba3eeae8aad857d442e2c220ee8fb9d163d2094effe5e2b5caaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d52c0a42000c08e48c92bca0cb052efe5fe4c425c94f38928e03a760d35c27a`

```dockerfile
```

-	Layers:
	-	`sha256:417cb0c8593799bfc188df240164693386c9ddfaa96d2ab8b1617c6bc857bed2`  
		Last Modified: Tue, 18 Mar 2025 05:32:13 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json
