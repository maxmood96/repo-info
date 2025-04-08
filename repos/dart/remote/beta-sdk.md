## `dart:beta-sdk`

```console
$ docker pull dart@sha256:4ccb6f37eb6ec7717a5ad816d923ec182c8db42bdbcd78ce2e113b87f7f28628
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
$ docker pull dart@sha256:1e274d9b7c9910144a884f867645f65f61088818d2ea7d69485193498e15edc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.2 MB (222241180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d7e5bc779d20f8133aa2f85d95243c5b400f16dd8ef87d2fda55edcc9eab9bc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Mar 2025 13:16:06 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb612903ca200110c7f7f770d9fc237f79154192b763a1e934f587e3f58ad5c5`  
		Last Modified: Tue, 08 Apr 2025 07:42:58 GMT  
		Size: 49.6 MB (49561029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fbb3a1dc4b06060e260de0cdca75a1dbd4d88c22e1b7b63c116f28dd4168fd`  
		Last Modified: Tue, 08 Apr 2025 07:42:57 GMT  
		Size: 1.2 MB (1221939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd271940f5cfbf9160be918ebea37eeced0f893fa3af28b4d983015f81074795`  
		Last Modified: Tue, 08 Apr 2025 07:43:52 GMT  
		Size: 147.5 MB (147520313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:adb066b2c7bd9cb1719b9fe89f08d56ba9675ff25b50791f714258bdaf8e09d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad70d97c2625773e8deadfa74011bbcc0d00324fabb06ae5636acaceec1aca2`

```dockerfile
```

-	Layers:
	-	`sha256:c5fc11dbabe7367166a5aab0f0d71715649fa7e8350bdf0da8a7769790b993cd`  
		Last Modified: Tue, 08 Apr 2025 07:43:48 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:521192f420b35b74bbed000e8a1871f5e203545a49afa6d0c097fb240228747f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295707207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0efea3cdc8df2bd1710b49d3ec0781604122cc7bbd454f2559c6a7bd0e365d5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Mar 2025 13:16:06 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80bbb59b3c6d28b1d12944a3bee25df2c8f2955bc3ddef68bb09ecc6bd8a27f`  
		Last Modified: Tue, 08 Apr 2025 06:10:13 GMT  
		Size: 54.7 MB (54678925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eadc9242253f4f40f913890c431fb0d0555540314635fafcc66af862303553c`  
		Last Modified: Tue, 08 Apr 2025 06:10:11 GMT  
		Size: 1.5 MB (1488222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd0007e812eaf3c30865e7188ddb5b304abf3b8f057a7e407cfcc434d187ea9`  
		Last Modified: Tue, 08 Apr 2025 06:11:07 GMT  
		Size: 211.5 MB (211473708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6e82a2433fafdca1a54168d653c5e13002a2e47b0246c92f9846c9bd97057c45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30245c7d71917665a7b5810cbd6f780e6661aa711af6764d021e02664b9d20a1`

```dockerfile
```

-	Layers:
	-	`sha256:918d2c63e9d3f645df872b6d24fc8810c193d2bb680977f762673a605f5cd867`  
		Last Modified: Tue, 08 Apr 2025 06:11:00 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json
