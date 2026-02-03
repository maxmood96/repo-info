## `dart:beta-sdk`

```console
$ docker pull dart@sha256:529aac689200d288054bb86c90c4e63068da441ea78e3f1d4ab0ae67116bd30e
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
$ docker pull dart@sha256:ec7c6c21a658c4a459272671bdb40ef856e772ef51a620c8e68f8f82491e26dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307092300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb4a87c46604e8f0e6fd9f552e6a5e24ace030dfcbf879aeaabbd9cd38a7df8f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 18:09:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 18:09:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 03 Feb 2026 18:09:33 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 03 Feb 2026 18:09:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 18:09:33 GMT
WORKDIR /root
# Tue, 03 Feb 2026 18:09:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=eb9219df3dd42f13ef890bbfb0b68a635abae5b749d6bfe4ce9295e03c72cfe4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=075a1ae7671259f50ae82df7e9d95917ac39d0253612e69e030bf55a8d382886;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f42a844c29c593569053baf722a65df0ae63d3a76e3c90ef0604edd8a9f0297d;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e35901b2ae4b20343be9acd6cdb13984597e097398616f66a4567cc0c18df4d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.5.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054b2f8d22b5c0c8dae9e2a9f50f8ff0f71c4227ccc877511e8edc0b9f14e387`  
		Last Modified: Tue, 03 Feb 2026 18:10:17 GMT  
		Size: 42.5 MB (42494595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a836a951a9210361b0f94cdf46cbbe13b86512c13065daaa1865bd535611de`  
		Last Modified: Tue, 03 Feb 2026 18:10:15 GMT  
		Size: 1.9 MB (1870170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8910b49fdf3d93aa73ba0e6b429ee53715f5c65546d03ddb1403b76b06a7c09`  
		Last Modified: Tue, 03 Feb 2026 18:10:21 GMT  
		Size: 232.9 MB (232948907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:86d482a787cf9a422e4e69558313202b9e6bd4d6f45dc98d110bc488a5f4a79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e652c961b293c9aa1eecfb44969d5ccb5e58e4bb7f7ad23d4532b8f2b0858dc`

```dockerfile
```

-	Layers:
	-	`sha256:357c94ccb27e6471a501a9be5a8f78a5ef7a2685c6666af2f52b26cc00d22ad2`  
		Last Modified: Tue, 03 Feb 2026 18:10:15 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:82b407b388868a6a3a49d21de4051be46e0e88493311696ed77b63196061e8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222905887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37438b18103d5f88e26a1bce47b80f6dd2e00c03b779d6b1b73bf9d38ad8009`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 18:07:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 18:07:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 03 Feb 2026 18:07:38 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 03 Feb 2026 18:07:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 18:07:38 GMT
WORKDIR /root
# Tue, 03 Feb 2026 18:08:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=eb9219df3dd42f13ef890bbfb0b68a635abae5b749d6bfe4ce9295e03c72cfe4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=075a1ae7671259f50ae82df7e9d95917ac39d0253612e69e030bf55a8d382886;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f42a844c29c593569053baf722a65df0ae63d3a76e3c90ef0604edd8a9f0297d;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e35901b2ae4b20343be9acd6cdb13984597e097398616f66a4567cc0c18df4d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.5.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bddbff6cd1a4e7530ba92a82b5fa316c38a394ea64bcf991e332404751ec977`  
		Last Modified: Tue, 03 Feb 2026 18:08:07 GMT  
		Size: 37.5 MB (37497525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3544cd714c9852937d3c1f1bbe3441f8b363f69df1cf88b74c50518c73979bcf`  
		Last Modified: Tue, 03 Feb 2026 18:08:06 GMT  
		Size: 1.3 MB (1273163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592722e36ce30cf565f0f3fd5848ee98cf2079785a50733006876c91fe75eace`  
		Last Modified: Tue, 03 Feb 2026 18:08:47 GMT  
		Size: 157.9 MB (157921419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8d4beeb66fa70ecdc25ec6ac50377061aef3537d2cd25bd03d9182629912ad83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9aed662de67cfc287c2417dfeb9702f5cb68faaa088eaf925c1d887ffbe71c`

```dockerfile
```

-	Layers:
	-	`sha256:f9c5b937d6228d6ba1327fa36c107232e555725c34d0d150950468f044c41b25`  
		Last Modified: Tue, 03 Feb 2026 18:08:43 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d364653776af18b5d6c1608795208fa38e291f8b5fd4478ba7aac8dfdac638f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305449882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18cd011e7d28fe19bc65162cf80a2bde6974f40a362d7ff66404b3ea805e46cd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 18:08:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 18:08:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 03 Feb 2026 18:08:35 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 03 Feb 2026 18:08:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 18:08:35 GMT
WORKDIR /root
# Tue, 03 Feb 2026 18:08:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=eb9219df3dd42f13ef890bbfb0b68a635abae5b749d6bfe4ce9295e03c72cfe4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=075a1ae7671259f50ae82df7e9d95917ac39d0253612e69e030bf55a8d382886;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f42a844c29c593569053baf722a65df0ae63d3a76e3c90ef0604edd8a9f0297d;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e35901b2ae4b20343be9acd6cdb13984597e097398616f66a4567cc0c18df4d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.5.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bd89ac57a49e667bd3e4487e4b0f642355c1cb80437ed839f6ee07f70608f1`  
		Last Modified: Tue, 03 Feb 2026 18:09:20 GMT  
		Size: 42.3 MB (42293808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee212405e94a4503a0777fa8b6d2fe0fe6a5ae6a09579e1e3c6ff7b62be3878`  
		Last Modified: Tue, 03 Feb 2026 18:09:18 GMT  
		Size: 1.6 MB (1564528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50be5dc433ee41adcc04d9d8e7dec37f5453b0e0b0811d980f32aa764b0c255`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 231.5 MB (231451450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a29a204afb75ec1c39ea4f35c3efeff3191cb321c3f7f3c2a367eac7a8176e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7778ef2d035d647bce92b3f04b00eeb610845a5d0ce04d3d7f8d9f0bfd72565f`

```dockerfile
```

-	Layers:
	-	`sha256:8a1b2e1c8e5ec5813fc803c41186be9ef851cf42bc6e8598fb89daff16fe04c1`  
		Last Modified: Tue, 03 Feb 2026 18:09:18 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:21b0280198017b02f30e648d88004010f7600e759f3e9cf9ae1e687fbab94972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251882011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453ee3791c857759be9f9511d851ae92b39357e45a774c9e324135b20c726c75`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Thu, 22 Jan 2026 06:09:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Jan 2026 06:09:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 22 Jan 2026 06:09:03 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 22 Jan 2026 06:09:03 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 06:09:03 GMT
WORKDIR /root
# Thu, 22 Jan 2026 06:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c33e9db6593e3ea9b06992a83d404099e1d3da4888651483a67d8c1debc6580;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4809981696ab4aa3898ca0e58f209d38df564d31b379c76312f23eda7efb9b44;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d6e641bbfadebb9ac490177f8e16978a01e964946adb592058fb27efbbbaf4c9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=36e5ebe20a6e8937ba85ead78dbf9335748175fbcf7c4ad6ae8dc84c02ecc91f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd964154fd69474bb760acc185c93887153305690d52ca95e5344f66cfc9735f`  
		Last Modified: Thu, 22 Jan 2026 06:14:10 GMT  
		Size: 41.6 MB (41560975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1a3e2e2795c7ed75e644f823196653ca7d26369e21df079bc51ff3212f1e11`  
		Last Modified: Thu, 22 Jan 2026 06:13:59 GMT  
		Size: 1.6 MB (1564661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716b12846ec2225948bdd9736fafb7b5d522aa5651e218eece0d7284456441e5`  
		Last Modified: Thu, 22 Jan 2026 06:14:32 GMT  
		Size: 180.5 MB (180484656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0dc8585dae936299ac8e380b29c78108e2b3df7d81edfa19fbada47b742132e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dfc0b09c9d9da734b208364407804d31d4996b034b7a84e6e097ae66b429794`

```dockerfile
```

-	Layers:
	-	`sha256:29bffaca319258079f9b4a77c56b8c29e5bb2093679f9d7c57d88c8c5913c250`  
		Last Modified: Thu, 22 Jan 2026 06:13:58 GMT  
		Size: 19.0 KB (18970 bytes)  
		MIME: application/vnd.in-toto+json
