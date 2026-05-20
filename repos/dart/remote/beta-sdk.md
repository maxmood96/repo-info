## `dart:beta-sdk`

```console
$ docker pull dart@sha256:5531be831e7d755f2dfe77d93f283cc35d300a1531e200a0b8c46505abdd31d4
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
$ docker pull dart@sha256:d81104c75faa61e9bc592dc7cc60c8ab4ffcb12db5371ab6e9ddc6992462751e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311868471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92de4785610143ad324146e9b88ed54133f6b2b3722461a075c76875e3d0ead`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:24:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:24:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 19 May 2026 23:24:01 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 19 May 2026 23:24:01 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:24:01 GMT
WORKDIR /root
# Tue, 19 May 2026 23:24:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2637e16c6e09ec72d1e2ae554f5b644f89bf58785dd17b2d9e09d216775e7b0`  
		Last Modified: Tue, 19 May 2026 23:24:45 GMT  
		Size: 42.5 MB (42504587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0391b9c8117291502f7211c501b407679110af6571981a1b1e68741437216bf3`  
		Last Modified: Tue, 19 May 2026 23:24:43 GMT  
		Size: 1.9 MB (1869784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b407e03bd03922c379b45fd3462ef310cff5c7f7656d368f78c7de49da7056`  
		Last Modified: Tue, 19 May 2026 23:24:49 GMT  
		Size: 237.7 MB (237714142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7c9a6af0d2e5c71425a48670acff41349acce81bb7731ee16a2dcba6e401e319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478e75cee0184f8913737b51ea4b7c4b15a1c8f6329b67a6aa083130e7c6b432`

```dockerfile
```

-	Layers:
	-	`sha256:5ae6f270b49f3ebfa43ab75a653087be14e198f81706b609bc2466946a28adde`  
		Last Modified: Tue, 19 May 2026 23:24:43 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:e0637ace0c2e5d05a184f5e0a6047e21b059fad18da985c1d6da20e5e2e4c84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226609126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23ccadca45cbbe6f1fbc13be8aa3315872ae4492f06e922250266627c10547a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:45:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:45:20 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:45:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:45:20 GMT
WORKDIR /root
# Fri, 08 May 2026 19:45:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c397f78e7cc2537e75904f25729ec5dba7faef504c3e5c252d1a5002cb7b51`  
		Last Modified: Fri, 08 May 2026 19:45:51 GMT  
		Size: 37.5 MB (37495343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f6665a0d68a8f335082af00f76179f9edc46554e97b0d1b653c7e52bdf9293`  
		Last Modified: Fri, 08 May 2026 19:45:49 GMT  
		Size: 1.3 MB (1273160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47abf148c5b483759071bc1a739e4bd39ad00582e479db7508632b941aee80ea`  
		Last Modified: Fri, 08 May 2026 19:45:54 GMT  
		Size: 161.6 MB (161625679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ba00119c541b5bbccf496d853b6c3d0e455f25c3a382bce4ff63f6efcca9ca97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b0302ae0294b448ee831ac5b8d8af4afdb677362938a9558aaec95c9c0ed90`

```dockerfile
```

-	Layers:
	-	`sha256:a4a8db3dac533e52d15d9938f2e60f68193e58194ae649f168595f25726b0afb`  
		Last Modified: Fri, 08 May 2026 19:45:49 GMT  
		Size: 19.0 KB (19027 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:50d7147ffd3c2564de733ed9dfa5e75c9a02716f4385168f3118afe434ba8869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310470172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92690a571315c8c8c9611c21ebb8d2203c2be96e084e23754d7dbc5f82abcf2d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 19 May 2026 23:27:34 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 19 May 2026 23:27:34 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:27:34 GMT
WORKDIR /root
# Tue, 19 May 2026 23:27:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd9eeb40aab4c60256acbfa8620c6a9f0c376405fa0b1fa38151ae5c49a76fc`  
		Last Modified: Tue, 19 May 2026 23:28:19 GMT  
		Size: 42.3 MB (42285492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5ae340b2688c04af9ea257dff8fbc380201889d785011cf78e8365b4f8ee89`  
		Last Modified: Tue, 19 May 2026 23:28:17 GMT  
		Size: 1.6 MB (1564379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d57db52b85afca7d5c6f5c60d44beaf0167c0dc1575e6ab0b0cee7434496e7a`  
		Last Modified: Tue, 19 May 2026 23:28:23 GMT  
		Size: 236.5 MB (236478350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:84e3bdd1ad43f42e59bb613ebbf32b943d5afe370bf297f1e24fa61b8ff6acb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eafd012745fa7c99f78132341076804da9c867806414fda3c2170806fa8f92d2`

```dockerfile
```

-	Layers:
	-	`sha256:0982a19342bf0fcd1105f96915f3307e4982172758aaa087f4f087b4a9781f6e`  
		Last Modified: Tue, 19 May 2026 23:28:17 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:6e7f3bf208fc36edb717cde32b6f70d8ef762f7fa7e461ea6abe3843c5c65900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249070092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d14d3055c105f6e5407b3ac58d6e3a71b650af4acb5c3657cd1aedfb72c4a8e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 01:09:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 01:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 11 May 2026 01:09:36 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 11 May 2026 01:09:36 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 01:09:36 GMT
WORKDIR /root
# Mon, 11 May 2026 01:16:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d634a513fcd794ececd26147a98618b5c5221ff1c54868c7b6e5b6da4652926`  
		Last Modified: Mon, 11 May 2026 01:14:52 GMT  
		Size: 41.6 MB (41571482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a9adbb6515f8ccbf983504652539ee3cd1ba5b6f18ce411b7ae7f68a3fc25d`  
		Last Modified: Mon, 11 May 2026 01:14:40 GMT  
		Size: 1.6 MB (1564400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07d4e7505852f448a449ce5385d217bd87481d51c1d4f0c1b0bc1f90f765b77`  
		Last Modified: Mon, 11 May 2026 01:21:11 GMT  
		Size: 177.7 MB (177653946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:cd48c5becbeb0db15a2a2441b58c53873edca8f21ba58946f83667ca9ce3a692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9faeabd8102b65f8c817c09d44e0e0dee141bfd47ff363f18cfe63b304c0d3e6`

```dockerfile
```

-	Layers:
	-	`sha256:3c205f87b681476829b897eb4f83b32f207072f29e3a36a516b5e5eee33e024c`  
		Last Modified: Mon, 11 May 2026 01:20:44 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json
