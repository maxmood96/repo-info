## `dart:latest`

```console
$ docker pull dart@sha256:323c2708601e0e6bb5303b40c68cd3550278afed190cc19dbfc7ce0d49005462
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
$ docker pull dart@sha256:a65a122371697a370b0d92494153849b975a1b3b31439d5e00a10adc1cb68cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307078454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d716c55938b238835332951a00bd2eb59ba6d2ee453f7116b9330cbcce0944`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:21:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:21:54 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:21:54 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:22:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1cca34bbfa78544772171ad6feb31a703cdfcf16bd7c4bcb7887be1a80847e`  
		Last Modified: Tue, 24 Feb 2026 19:22:33 GMT  
		Size: 42.5 MB (42492297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096946df2b65a1445800d274da6d6d968eff32522f27fa501c1ffe41b68a3e49`  
		Last Modified: Tue, 24 Feb 2026 19:22:31 GMT  
		Size: 1.9 MB (1870163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad851a2efa89a226d1dd2de3c2ee267ceceecd4af60a25fa03fe99e33b7e71ec`  
		Last Modified: Tue, 24 Feb 2026 19:22:37 GMT  
		Size: 232.9 MB (232937330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:8faf56f2168cec7a44f4dd88c7503275c17e3f418cdeb65bb8a47efa7aaaff34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219b6af7f53ec82afc087f7a93c977ea0fe2ed30b56e484a88d980e8ee572ee4`

```dockerfile
```

-	Layers:
	-	`sha256:d24dc0dfdb2fff39856f19b0f469413dc9acd620f72c8e9c0c3a5a11170ea53c`  
		Last Modified: Tue, 24 Feb 2026 19:22:31 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:9b51681f24ce0021c7425228dff567d12ea224cbe1c4d92ea8a91460b5cb2b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222903041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144150cff24fee0d4e64effbe4d507924f146c6338cb1f95a74ebbec1319801d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:08:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 20:08:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:08:02 GMT
WORKDIR /root
# Tue, 24 Feb 2026 20:08:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6c691e32f18bfa78558b54a419af4c094ac4f646129f5a304d57094b3a133e`  
		Last Modified: Tue, 24 Feb 2026 20:08:30 GMT  
		Size: 37.5 MB (37494610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6dccb597ee6ded5ec69bb8232a71a0dac91030b7b89cc91e30a4617716c2a`  
		Last Modified: Tue, 24 Feb 2026 20:08:29 GMT  
		Size: 1.3 MB (1273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f78bc4992a9cc0a71ad4359e45d32c02e836e66b1f18908ea46a8643f30a61`  
		Last Modified: Tue, 24 Feb 2026 20:08:33 GMT  
		Size: 157.9 MB (157921498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:f83ec5644f8b2b5c3c8c3c9c8641f3c517bd29eef1a10422e7fd7cf3ea625a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fa860ebbe31412d1b796484530c8977632f46901c40e959b5954b17b0aeb72`

```dockerfile
```

-	Layers:
	-	`sha256:9cad6fbe4758047e7694049f647722cb6fac1d7998a8ba88238059ecb934aefc`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:75b7d635e8017bedfb7558b673e86d06d296c5e2e4928094d361dea08a2e33d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305432790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08262d25efa06630d26613096ad8569fcbae1e4a76c6282c25b7fed371ff2c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:26:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:26:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:26:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:26:13 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:26:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0817a6b12277453cbb8c6769167bda699e33a67c6b6f7728471333fd409234b0`  
		Last Modified: Tue, 24 Feb 2026 19:26:52 GMT  
		Size: 42.3 MB (42291780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fd117eca6678bea966f82c3670c899371d76ab1831faf88cca36aba6a9b152`  
		Last Modified: Tue, 24 Feb 2026 19:26:50 GMT  
		Size: 1.6 MB (1564525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974025aa8251e00a687a16e8110c92efa7be829da96a4fc60097c79eba30b243`  
		Last Modified: Tue, 24 Feb 2026 19:26:56 GMT  
		Size: 231.4 MB (231436355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:41f5ea01f073f96696a4d8066ab95d06db8ce516293223eef647fe73f5cdf873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcac1eeaf18c60b98ddb7c4a70d4c07f54262ee40fe793278c498cf642574f0`

```dockerfile
```

-	Layers:
	-	`sha256:ec630e8c02811815587c511be77ff5b26e883a970894a3cac50f4178a4c75d49`  
		Last Modified: Tue, 24 Feb 2026 19:26:50 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; riscv64

```console
$ docker pull dart@sha256:f157748aa920b9240a8546e6a1d5de4a9ae52a15b79d40a108478961a48055b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f723dfeef183dcfa3b0acf8fcc88706ff55dbb45569e3c286bd844322006a68`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Tue, 24 Feb 2026 17:36:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 17:36:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 17:36:22 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 17:36:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 17:36:22 GMT
WORKDIR /root
# Tue, 24 Feb 2026 17:37:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b1ffb5d54515c9205f5aa5b80f611aabd2400fab85d7920cddf64ce77f4b24`  
		Last Modified: Tue, 24 Feb 2026 17:41:27 GMT  
		Size: 41.6 MB (41560908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d700e76008c419c1f10155a84068cb1db35d3aa1389becf195da577452287ba5`  
		Last Modified: Tue, 24 Feb 2026 17:41:14 GMT  
		Size: 1.6 MB (1564666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35de2c7d0e6f4c8d6fd328706d63544c261f9273af7cb62c798e9b82b8ba8f42`  
		Last Modified: Tue, 24 Feb 2026 17:41:48 GMT  
		Size: 180.5 MB (180483769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:c3ea28c525d10de65898680866649a2912f84fbff8393e2cba0ecd95f02062dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c4fa45add5a846f49af93da14a163f74f5a76d0a79c3d817b18c571a4723cf`

```dockerfile
```

-	Layers:
	-	`sha256:57497dccfd171bb609a59bbac9b901da0d1286c242658b791c28b340daa90db7`  
		Last Modified: Tue, 24 Feb 2026 17:41:14 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json
