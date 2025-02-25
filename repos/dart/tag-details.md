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
$ docker pull dart@sha256:9fb41fc1eefdf432694e17b0f80c9135b1f79dd3f645c403f98ed5ae71799c36
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
$ docker pull dart@sha256:b43c3f563f15dddf5e962075c1faddfebe1a094b6144718e65a1706cb5b28951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304966717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb5db526fd50d343e0012bb9386d775dd776a8eda76e18672ead7a5a7f5cabb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c7a891ed4d4ce462192c75f6acfaaa58a1da6eb029e83aa11eb66544552f7c`  
		Last Modified: Tue, 25 Feb 2025 03:22:22 GMT  
		Size: 54.9 MB (54906829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774f8223e39d93a20bddd53031475c142c44e17195a7f12b6c598e2db7e9907a`  
		Last Modified: Tue, 25 Feb 2025 03:22:20 GMT  
		Size: 1.8 MB (1796915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d1765a8b4993ff038f8e0c1b88d3cbb5ed04d215a238ae34a65c855a1a33a7`  
		Last Modified: Tue, 25 Feb 2025 03:22:26 GMT  
		Size: 220.0 MB (220043640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:169df6ff0e0981d81b3bb4d11e57b6a80b53331b023269151337081683e46041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8cb0ea4652d056835eef3e5f7dfc152ec0d53e1c802bbc00f28938bf765cc60`

```dockerfile
```

-	Layers:
	-	`sha256:7d677a1352e3e2dd50ea7d03c7b98fdfab0a02c53b7b95e3a2330691360aea1e`  
		Last Modified: Tue, 25 Feb 2025 03:22:20 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:febe29a2dbb15f1af5716b8e31db5df7726b12d0e05688bb64e305eba8627f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226300684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747b24a70e7d9017ee70e379389b8ee87f7c8595ae17649befdce5d789459b88`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5237f7e72c8f2131b9cde5d18f813ca79c323e6d50dcb0ee952dbf3febbdec40`  
		Last Modified: Tue, 25 Feb 2025 07:22:07 GMT  
		Size: 49.6 MB (49561814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0977386395adb5a5e238be6fc311e9c36206d68fd7d29b986b77d1ae9a968bbb`  
		Last Modified: Tue, 25 Feb 2025 07:22:05 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3b45e78f7fe8dc51f123bb726524bd6c8d6e5245ad42836bd0fd1b3b5b2b26`  
		Last Modified: Tue, 25 Feb 2025 13:41:48 GMT  
		Size: 151.6 MB (151597429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:1af9585a83934e03ab0677a55db0ed0922fd0c0baecccf06d373d6b08743fe1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4370e355c021d94d848ea7dea1197e02c234163c22c087eeb771b2ad7efe4570`

```dockerfile
```

-	Layers:
	-	`sha256:beea83ecd2bbc9359497d0fb39ca7a8adf3af6bfe66b08574f61581607b228a9`  
		Last Modified: Tue, 25 Feb 2025 13:41:44 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:9cf616067bcbd55ae946d8f559b0ce971cf8773aa95de21187ee844f1317e05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303823647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ae015985756d0b209352bb079df8905fb1b3f933e07ed72266c8d95f9cb226`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80522afdd70276ee5ecab6e21fe3c0f9d8d1314ec31a717386aa86ec42d2fae4`  
		Last Modified: Tue, 25 Feb 2025 05:48:31 GMT  
		Size: 54.7 MB (54677020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443988cca47e542f6b4f11adb471ee7e46e5135c4faf5cb541eb2117c1437ebd`  
		Last Modified: Tue, 25 Feb 2025 05:48:29 GMT  
		Size: 1.5 MB (1488025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790f1ce84f87eace2e2834f6fb45d00c3c0da18abb45fe361e7919ef6d3f703e`  
		Last Modified: Tue, 25 Feb 2025 05:48:36 GMT  
		Size: 219.6 MB (219610145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:29102ee6a46ac1024761115e544098a021cc3632a3ba2d23bfaf1b92b8e4d133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5ed1c6b1c90f53adfed73e2e5398a7228564b1e89332dfcb8cf983337b89b6`

```dockerfile
```

-	Layers:
	-	`sha256:0d5bd9b1b0abac9c7743438d0f786399f3555ccd6b5a945f2e5f043b789d87cf`  
		Last Modified: Tue, 25 Feb 2025 05:48:29 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:9fb41fc1eefdf432694e17b0f80c9135b1f79dd3f645c403f98ed5ae71799c36
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
$ docker pull dart@sha256:b43c3f563f15dddf5e962075c1faddfebe1a094b6144718e65a1706cb5b28951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304966717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb5db526fd50d343e0012bb9386d775dd776a8eda76e18672ead7a5a7f5cabb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c7a891ed4d4ce462192c75f6acfaaa58a1da6eb029e83aa11eb66544552f7c`  
		Last Modified: Tue, 25 Feb 2025 03:22:22 GMT  
		Size: 54.9 MB (54906829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774f8223e39d93a20bddd53031475c142c44e17195a7f12b6c598e2db7e9907a`  
		Last Modified: Tue, 25 Feb 2025 03:22:20 GMT  
		Size: 1.8 MB (1796915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d1765a8b4993ff038f8e0c1b88d3cbb5ed04d215a238ae34a65c855a1a33a7`  
		Last Modified: Tue, 25 Feb 2025 03:22:26 GMT  
		Size: 220.0 MB (220043640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:169df6ff0e0981d81b3bb4d11e57b6a80b53331b023269151337081683e46041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8cb0ea4652d056835eef3e5f7dfc152ec0d53e1c802bbc00f28938bf765cc60`

```dockerfile
```

-	Layers:
	-	`sha256:7d677a1352e3e2dd50ea7d03c7b98fdfab0a02c53b7b95e3a2330691360aea1e`  
		Last Modified: Tue, 25 Feb 2025 03:22:20 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:febe29a2dbb15f1af5716b8e31db5df7726b12d0e05688bb64e305eba8627f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226300684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747b24a70e7d9017ee70e379389b8ee87f7c8595ae17649befdce5d789459b88`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5237f7e72c8f2131b9cde5d18f813ca79c323e6d50dcb0ee952dbf3febbdec40`  
		Last Modified: Tue, 25 Feb 2025 07:22:07 GMT  
		Size: 49.6 MB (49561814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0977386395adb5a5e238be6fc311e9c36206d68fd7d29b986b77d1ae9a968bbb`  
		Last Modified: Tue, 25 Feb 2025 07:22:05 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3b45e78f7fe8dc51f123bb726524bd6c8d6e5245ad42836bd0fd1b3b5b2b26`  
		Last Modified: Tue, 25 Feb 2025 13:41:48 GMT  
		Size: 151.6 MB (151597429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1af9585a83934e03ab0677a55db0ed0922fd0c0baecccf06d373d6b08743fe1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4370e355c021d94d848ea7dea1197e02c234163c22c087eeb771b2ad7efe4570`

```dockerfile
```

-	Layers:
	-	`sha256:beea83ecd2bbc9359497d0fb39ca7a8adf3af6bfe66b08574f61581607b228a9`  
		Last Modified: Tue, 25 Feb 2025 13:41:44 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:9cf616067bcbd55ae946d8f559b0ce971cf8773aa95de21187ee844f1317e05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303823647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ae015985756d0b209352bb079df8905fb1b3f933e07ed72266c8d95f9cb226`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80522afdd70276ee5ecab6e21fe3c0f9d8d1314ec31a717386aa86ec42d2fae4`  
		Last Modified: Tue, 25 Feb 2025 05:48:31 GMT  
		Size: 54.7 MB (54677020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443988cca47e542f6b4f11adb471ee7e46e5135c4faf5cb541eb2117c1437ebd`  
		Last Modified: Tue, 25 Feb 2025 05:48:29 GMT  
		Size: 1.5 MB (1488025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790f1ce84f87eace2e2834f6fb45d00c3c0da18abb45fe361e7919ef6d3f703e`  
		Last Modified: Tue, 25 Feb 2025 05:48:36 GMT  
		Size: 219.6 MB (219610145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:29102ee6a46ac1024761115e544098a021cc3632a3ba2d23bfaf1b92b8e4d133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5ed1c6b1c90f53adfed73e2e5398a7228564b1e89332dfcb8cf983337b89b6`

```dockerfile
```

-	Layers:
	-	`sha256:0d5bd9b1b0abac9c7743438d0f786399f3555ccd6b5a945f2e5f043b789d87cf`  
		Last Modified: Tue, 25 Feb 2025 05:48:29 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.7`

```console
$ docker pull dart@sha256:9fb41fc1eefdf432694e17b0f80c9135b1f79dd3f645c403f98ed5ae71799c36
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
$ docker pull dart@sha256:b43c3f563f15dddf5e962075c1faddfebe1a094b6144718e65a1706cb5b28951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304966717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb5db526fd50d343e0012bb9386d775dd776a8eda76e18672ead7a5a7f5cabb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c7a891ed4d4ce462192c75f6acfaaa58a1da6eb029e83aa11eb66544552f7c`  
		Last Modified: Tue, 25 Feb 2025 03:22:22 GMT  
		Size: 54.9 MB (54906829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774f8223e39d93a20bddd53031475c142c44e17195a7f12b6c598e2db7e9907a`  
		Last Modified: Tue, 25 Feb 2025 03:22:20 GMT  
		Size: 1.8 MB (1796915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d1765a8b4993ff038f8e0c1b88d3cbb5ed04d215a238ae34a65c855a1a33a7`  
		Last Modified: Tue, 25 Feb 2025 03:22:26 GMT  
		Size: 220.0 MB (220043640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7` - unknown; unknown

```console
$ docker pull dart@sha256:169df6ff0e0981d81b3bb4d11e57b6a80b53331b023269151337081683e46041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8cb0ea4652d056835eef3e5f7dfc152ec0d53e1c802bbc00f28938bf765cc60`

```dockerfile
```

-	Layers:
	-	`sha256:7d677a1352e3e2dd50ea7d03c7b98fdfab0a02c53b7b95e3a2330691360aea1e`  
		Last Modified: Tue, 25 Feb 2025 03:22:20 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7` - linux; arm variant v7

```console
$ docker pull dart@sha256:febe29a2dbb15f1af5716b8e31db5df7726b12d0e05688bb64e305eba8627f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226300684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747b24a70e7d9017ee70e379389b8ee87f7c8595ae17649befdce5d789459b88`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5237f7e72c8f2131b9cde5d18f813ca79c323e6d50dcb0ee952dbf3febbdec40`  
		Last Modified: Tue, 25 Feb 2025 07:22:07 GMT  
		Size: 49.6 MB (49561814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0977386395adb5a5e238be6fc311e9c36206d68fd7d29b986b77d1ae9a968bbb`  
		Last Modified: Tue, 25 Feb 2025 07:22:05 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3b45e78f7fe8dc51f123bb726524bd6c8d6e5245ad42836bd0fd1b3b5b2b26`  
		Last Modified: Tue, 25 Feb 2025 13:41:48 GMT  
		Size: 151.6 MB (151597429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7` - unknown; unknown

```console
$ docker pull dart@sha256:1af9585a83934e03ab0677a55db0ed0922fd0c0baecccf06d373d6b08743fe1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4370e355c021d94d848ea7dea1197e02c234163c22c087eeb771b2ad7efe4570`

```dockerfile
```

-	Layers:
	-	`sha256:beea83ecd2bbc9359497d0fb39ca7a8adf3af6bfe66b08574f61581607b228a9`  
		Last Modified: Tue, 25 Feb 2025 13:41:44 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:9cf616067bcbd55ae946d8f559b0ce971cf8773aa95de21187ee844f1317e05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303823647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ae015985756d0b209352bb079df8905fb1b3f933e07ed72266c8d95f9cb226`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80522afdd70276ee5ecab6e21fe3c0f9d8d1314ec31a717386aa86ec42d2fae4`  
		Last Modified: Tue, 25 Feb 2025 05:48:31 GMT  
		Size: 54.7 MB (54677020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443988cca47e542f6b4f11adb471ee7e46e5135c4faf5cb541eb2117c1437ebd`  
		Last Modified: Tue, 25 Feb 2025 05:48:29 GMT  
		Size: 1.5 MB (1488025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790f1ce84f87eace2e2834f6fb45d00c3c0da18abb45fe361e7919ef6d3f703e`  
		Last Modified: Tue, 25 Feb 2025 05:48:36 GMT  
		Size: 219.6 MB (219610145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7` - unknown; unknown

```console
$ docker pull dart@sha256:29102ee6a46ac1024761115e544098a021cc3632a3ba2d23bfaf1b92b8e4d133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5ed1c6b1c90f53adfed73e2e5398a7228564b1e89332dfcb8cf983337b89b6`

```dockerfile
```

-	Layers:
	-	`sha256:0d5bd9b1b0abac9c7743438d0f786399f3555ccd6b5a945f2e5f043b789d87cf`  
		Last Modified: Tue, 25 Feb 2025 05:48:29 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.7-sdk`

```console
$ docker pull dart@sha256:9fb41fc1eefdf432694e17b0f80c9135b1f79dd3f645c403f98ed5ae71799c36
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
$ docker pull dart@sha256:b43c3f563f15dddf5e962075c1faddfebe1a094b6144718e65a1706cb5b28951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304966717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb5db526fd50d343e0012bb9386d775dd776a8eda76e18672ead7a5a7f5cabb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c7a891ed4d4ce462192c75f6acfaaa58a1da6eb029e83aa11eb66544552f7c`  
		Last Modified: Tue, 25 Feb 2025 03:22:22 GMT  
		Size: 54.9 MB (54906829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774f8223e39d93a20bddd53031475c142c44e17195a7f12b6c598e2db7e9907a`  
		Last Modified: Tue, 25 Feb 2025 03:22:20 GMT  
		Size: 1.8 MB (1796915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d1765a8b4993ff038f8e0c1b88d3cbb5ed04d215a238ae34a65c855a1a33a7`  
		Last Modified: Tue, 25 Feb 2025 03:22:26 GMT  
		Size: 220.0 MB (220043640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:169df6ff0e0981d81b3bb4d11e57b6a80b53331b023269151337081683e46041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8cb0ea4652d056835eef3e5f7dfc152ec0d53e1c802bbc00f28938bf765cc60`

```dockerfile
```

-	Layers:
	-	`sha256:7d677a1352e3e2dd50ea7d03c7b98fdfab0a02c53b7b95e3a2330691360aea1e`  
		Last Modified: Tue, 25 Feb 2025 03:22:20 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:febe29a2dbb15f1af5716b8e31db5df7726b12d0e05688bb64e305eba8627f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226300684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747b24a70e7d9017ee70e379389b8ee87f7c8595ae17649befdce5d789459b88`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5237f7e72c8f2131b9cde5d18f813ca79c323e6d50dcb0ee952dbf3febbdec40`  
		Last Modified: Tue, 25 Feb 2025 07:22:07 GMT  
		Size: 49.6 MB (49561814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0977386395adb5a5e238be6fc311e9c36206d68fd7d29b986b77d1ae9a968bbb`  
		Last Modified: Tue, 25 Feb 2025 07:22:05 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3b45e78f7fe8dc51f123bb726524bd6c8d6e5245ad42836bd0fd1b3b5b2b26`  
		Last Modified: Tue, 25 Feb 2025 13:41:48 GMT  
		Size: 151.6 MB (151597429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1af9585a83934e03ab0677a55db0ed0922fd0c0baecccf06d373d6b08743fe1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4370e355c021d94d848ea7dea1197e02c234163c22c087eeb771b2ad7efe4570`

```dockerfile
```

-	Layers:
	-	`sha256:beea83ecd2bbc9359497d0fb39ca7a8adf3af6bfe66b08574f61581607b228a9`  
		Last Modified: Tue, 25 Feb 2025 13:41:44 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:9cf616067bcbd55ae946d8f559b0ce971cf8773aa95de21187ee844f1317e05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303823647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ae015985756d0b209352bb079df8905fb1b3f933e07ed72266c8d95f9cb226`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80522afdd70276ee5ecab6e21fe3c0f9d8d1314ec31a717386aa86ec42d2fae4`  
		Last Modified: Tue, 25 Feb 2025 05:48:31 GMT  
		Size: 54.7 MB (54677020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443988cca47e542f6b4f11adb471ee7e46e5135c4faf5cb541eb2117c1437ebd`  
		Last Modified: Tue, 25 Feb 2025 05:48:29 GMT  
		Size: 1.5 MB (1488025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790f1ce84f87eace2e2834f6fb45d00c3c0da18abb45fe361e7919ef6d3f703e`  
		Last Modified: Tue, 25 Feb 2025 05:48:36 GMT  
		Size: 219.6 MB (219610145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:29102ee6a46ac1024761115e544098a021cc3632a3ba2d23bfaf1b92b8e4d133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5ed1c6b1c90f53adfed73e2e5398a7228564b1e89332dfcb8cf983337b89b6`

```dockerfile
```

-	Layers:
	-	`sha256:0d5bd9b1b0abac9c7743438d0f786399f3555ccd6b5a945f2e5f043b789d87cf`  
		Last Modified: Tue, 25 Feb 2025 05:48:29 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.7.0`

```console
$ docker pull dart@sha256:9fb41fc1eefdf432694e17b0f80c9135b1f79dd3f645c403f98ed5ae71799c36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.7.0` - linux; amd64

```console
$ docker pull dart@sha256:b43c3f563f15dddf5e962075c1faddfebe1a094b6144718e65a1706cb5b28951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304966717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb5db526fd50d343e0012bb9386d775dd776a8eda76e18672ead7a5a7f5cabb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c7a891ed4d4ce462192c75f6acfaaa58a1da6eb029e83aa11eb66544552f7c`  
		Last Modified: Tue, 25 Feb 2025 03:22:22 GMT  
		Size: 54.9 MB (54906829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774f8223e39d93a20bddd53031475c142c44e17195a7f12b6c598e2db7e9907a`  
		Last Modified: Tue, 25 Feb 2025 03:22:20 GMT  
		Size: 1.8 MB (1796915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d1765a8b4993ff038f8e0c1b88d3cbb5ed04d215a238ae34a65c855a1a33a7`  
		Last Modified: Tue, 25 Feb 2025 03:22:26 GMT  
		Size: 220.0 MB (220043640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.0` - unknown; unknown

```console
$ docker pull dart@sha256:169df6ff0e0981d81b3bb4d11e57b6a80b53331b023269151337081683e46041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8cb0ea4652d056835eef3e5f7dfc152ec0d53e1c802bbc00f28938bf765cc60`

```dockerfile
```

-	Layers:
	-	`sha256:7d677a1352e3e2dd50ea7d03c7b98fdfab0a02c53b7b95e3a2330691360aea1e`  
		Last Modified: Tue, 25 Feb 2025 03:22:20 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7.0` - linux; arm variant v7

```console
$ docker pull dart@sha256:febe29a2dbb15f1af5716b8e31db5df7726b12d0e05688bb64e305eba8627f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226300684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747b24a70e7d9017ee70e379389b8ee87f7c8595ae17649befdce5d789459b88`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5237f7e72c8f2131b9cde5d18f813ca79c323e6d50dcb0ee952dbf3febbdec40`  
		Last Modified: Tue, 25 Feb 2025 07:22:07 GMT  
		Size: 49.6 MB (49561814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0977386395adb5a5e238be6fc311e9c36206d68fd7d29b986b77d1ae9a968bbb`  
		Last Modified: Tue, 25 Feb 2025 07:22:05 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3b45e78f7fe8dc51f123bb726524bd6c8d6e5245ad42836bd0fd1b3b5b2b26`  
		Last Modified: Tue, 25 Feb 2025 13:41:48 GMT  
		Size: 151.6 MB (151597429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.0` - unknown; unknown

```console
$ docker pull dart@sha256:1af9585a83934e03ab0677a55db0ed0922fd0c0baecccf06d373d6b08743fe1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4370e355c021d94d848ea7dea1197e02c234163c22c087eeb771b2ad7efe4570`

```dockerfile
```

-	Layers:
	-	`sha256:beea83ecd2bbc9359497d0fb39ca7a8adf3af6bfe66b08574f61581607b228a9`  
		Last Modified: Tue, 25 Feb 2025 13:41:44 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7.0` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:9cf616067bcbd55ae946d8f559b0ce971cf8773aa95de21187ee844f1317e05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303823647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ae015985756d0b209352bb079df8905fb1b3f933e07ed72266c8d95f9cb226`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80522afdd70276ee5ecab6e21fe3c0f9d8d1314ec31a717386aa86ec42d2fae4`  
		Last Modified: Tue, 25 Feb 2025 05:48:31 GMT  
		Size: 54.7 MB (54677020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443988cca47e542f6b4f11adb471ee7e46e5135c4faf5cb541eb2117c1437ebd`  
		Last Modified: Tue, 25 Feb 2025 05:48:29 GMT  
		Size: 1.5 MB (1488025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790f1ce84f87eace2e2834f6fb45d00c3c0da18abb45fe361e7919ef6d3f703e`  
		Last Modified: Tue, 25 Feb 2025 05:48:36 GMT  
		Size: 219.6 MB (219610145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.0` - unknown; unknown

```console
$ docker pull dart@sha256:29102ee6a46ac1024761115e544098a021cc3632a3ba2d23bfaf1b92b8e4d133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5ed1c6b1c90f53adfed73e2e5398a7228564b1e89332dfcb8cf983337b89b6`

```dockerfile
```

-	Layers:
	-	`sha256:0d5bd9b1b0abac9c7743438d0f786399f3555ccd6b5a945f2e5f043b789d87cf`  
		Last Modified: Tue, 25 Feb 2025 05:48:29 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.7.0-sdk`

```console
$ docker pull dart@sha256:9fb41fc1eefdf432694e17b0f80c9135b1f79dd3f645c403f98ed5ae71799c36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.7.0-sdk` - linux; amd64

```console
$ docker pull dart@sha256:b43c3f563f15dddf5e962075c1faddfebe1a094b6144718e65a1706cb5b28951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304966717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb5db526fd50d343e0012bb9386d775dd776a8eda76e18672ead7a5a7f5cabb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c7a891ed4d4ce462192c75f6acfaaa58a1da6eb029e83aa11eb66544552f7c`  
		Last Modified: Tue, 25 Feb 2025 03:22:22 GMT  
		Size: 54.9 MB (54906829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774f8223e39d93a20bddd53031475c142c44e17195a7f12b6c598e2db7e9907a`  
		Last Modified: Tue, 25 Feb 2025 03:22:20 GMT  
		Size: 1.8 MB (1796915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d1765a8b4993ff038f8e0c1b88d3cbb5ed04d215a238ae34a65c855a1a33a7`  
		Last Modified: Tue, 25 Feb 2025 03:22:26 GMT  
		Size: 220.0 MB (220043640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.0-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:169df6ff0e0981d81b3bb4d11e57b6a80b53331b023269151337081683e46041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8cb0ea4652d056835eef3e5f7dfc152ec0d53e1c802bbc00f28938bf765cc60`

```dockerfile
```

-	Layers:
	-	`sha256:7d677a1352e3e2dd50ea7d03c7b98fdfab0a02c53b7b95e3a2330691360aea1e`  
		Last Modified: Tue, 25 Feb 2025 03:22:20 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7.0-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:febe29a2dbb15f1af5716b8e31db5df7726b12d0e05688bb64e305eba8627f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226300684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747b24a70e7d9017ee70e379389b8ee87f7c8595ae17649befdce5d789459b88`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5237f7e72c8f2131b9cde5d18f813ca79c323e6d50dcb0ee952dbf3febbdec40`  
		Last Modified: Tue, 25 Feb 2025 07:22:07 GMT  
		Size: 49.6 MB (49561814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0977386395adb5a5e238be6fc311e9c36206d68fd7d29b986b77d1ae9a968bbb`  
		Last Modified: Tue, 25 Feb 2025 07:22:05 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3b45e78f7fe8dc51f123bb726524bd6c8d6e5245ad42836bd0fd1b3b5b2b26`  
		Last Modified: Tue, 25 Feb 2025 13:41:48 GMT  
		Size: 151.6 MB (151597429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.0-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1af9585a83934e03ab0677a55db0ed0922fd0c0baecccf06d373d6b08743fe1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4370e355c021d94d848ea7dea1197e02c234163c22c087eeb771b2ad7efe4570`

```dockerfile
```

-	Layers:
	-	`sha256:beea83ecd2bbc9359497d0fb39ca7a8adf3af6bfe66b08574f61581607b228a9`  
		Last Modified: Tue, 25 Feb 2025 13:41:44 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7.0-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:9cf616067bcbd55ae946d8f559b0ce971cf8773aa95de21187ee844f1317e05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303823647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ae015985756d0b209352bb079df8905fb1b3f933e07ed72266c8d95f9cb226`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80522afdd70276ee5ecab6e21fe3c0f9d8d1314ec31a717386aa86ec42d2fae4`  
		Last Modified: Tue, 25 Feb 2025 05:48:31 GMT  
		Size: 54.7 MB (54677020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443988cca47e542f6b4f11adb471ee7e46e5135c4faf5cb541eb2117c1437ebd`  
		Last Modified: Tue, 25 Feb 2025 05:48:29 GMT  
		Size: 1.5 MB (1488025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790f1ce84f87eace2e2834f6fb45d00c3c0da18abb45fe361e7919ef6d3f703e`  
		Last Modified: Tue, 25 Feb 2025 05:48:36 GMT  
		Size: 219.6 MB (219610145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.0-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:29102ee6a46ac1024761115e544098a021cc3632a3ba2d23bfaf1b92b8e4d133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5ed1c6b1c90f53adfed73e2e5398a7228564b1e89332dfcb8cf983337b89b6`

```dockerfile
```

-	Layers:
	-	`sha256:0d5bd9b1b0abac9c7743438d0f786399f3555ccd6b5a945f2e5f043b789d87cf`  
		Last Modified: Tue, 25 Feb 2025 05:48:29 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8.0-70.1.beta`

```console
$ docker pull dart@sha256:6a3f40761c3fa74a597b4a6b077ae651cd87c02d1c15aa1aa6989030c5816095
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.8.0-70.1.beta` - linux; amd64

```console
$ docker pull dart@sha256:dbff64306425ea6f7ab495b68c8073277fe885b1aff37f0655e4d51dfb9fe94e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296644093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adbeea1840fd94bc8fb1e1b1f9aa2abc3b62430ded33ae6c7bda5990a687b71f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c1b1d66c0fd37a432b268e43b06520b824ada88b268e9e0a3d0e244ba4f3abe4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=38ccb0abd0f754a7d3b95106cdccd54899a749be7833e49455eadf689941256c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ce086fb32bceed703e6f460a1c9835aaa421b83ee960d6dfee809d527b5e09;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-70.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd64cbcb2255822a221780af272c9d9f03b9d7f0e178f5f6f37e41e7532d6a4`  
		Last Modified: Tue, 25 Feb 2025 02:13:57 GMT  
		Size: 54.9 MB (54906703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbe373cbcef45e6a19683de9449a5262c7468d5918f0a8a3120cae60ca66598`  
		Last Modified: Tue, 25 Feb 2025 02:13:56 GMT  
		Size: 1.8 MB (1796911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ed192a04e915894a60de10e507c9ffaff9c360ccfc8f66efa78e48608a4696`  
		Last Modified: Tue, 25 Feb 2025 02:14:01 GMT  
		Size: 211.7 MB (211721146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0-70.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:6bf2170c637ff046a22dac219dc0b4e9ea6b31281a9949d6f0fd9cc8dd143da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fd81d6a88a1f19640924a1e58b70b84cc799a0a1859b1cc94a42376c28d579`

```dockerfile
```

-	Layers:
	-	`sha256:2d3b87ba728f21d5219a8d61bba8f19039f8943261a7bb25e28e5aedb94e295e`  
		Last Modified: Tue, 25 Feb 2025 02:13:55 GMT  
		Size: 17.9 KB (17906 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.0-70.1.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:c031f2d72845f68e6558370848683261d9e75799af207c90bc41a0a62602f02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.3 MB (219315973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f787ee2dce46552a3e4edc390a8349514eff3dc6e772b6b9bebcdaf854ce6bc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c1b1d66c0fd37a432b268e43b06520b824ada88b268e9e0a3d0e244ba4f3abe4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=38ccb0abd0f754a7d3b95106cdccd54899a749be7833e49455eadf689941256c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ce086fb32bceed703e6f460a1c9835aaa421b83ee960d6dfee809d527b5e09;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-70.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5237f7e72c8f2131b9cde5d18f813ca79c323e6d50dcb0ee952dbf3febbdec40`  
		Last Modified: Tue, 25 Feb 2025 07:22:07 GMT  
		Size: 49.6 MB (49561814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0977386395adb5a5e238be6fc311e9c36206d68fd7d29b986b77d1ae9a968bbb`  
		Last Modified: Tue, 25 Feb 2025 07:22:05 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8291d9e33f2cacab92e8ac26e8a62fe150ce7178aed1445dc4d49aae993f18`  
		Last Modified: Tue, 25 Feb 2025 07:22:09 GMT  
		Size: 144.6 MB (144612718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0-70.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:3d855b21d7f2cc7261ceb05ed48ba9a132d4b7ae960750c272a967a1d414c97b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a76135a9102fdcb18cfbdc961b1514867f202bb32594480f423dbfd5240cdd`

```dockerfile
```

-	Layers:
	-	`sha256:77b17baa3d4085b12515992524200040bdd417c4a8531bed02b8e141e270083e`  
		Last Modified: Tue, 25 Feb 2025 07:22:05 GMT  
		Size: 18.0 KB (18008 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.0-70.1.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:7ec47a5bef9f97de020fd0bafa58712ecd96c1d28bfb6251650fc945c2010f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.6 MB (295554035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429d573a545a4dea83218d469bbfcd1c27de8963db715d742d0d60c8b3b187a0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c1b1d66c0fd37a432b268e43b06520b824ada88b268e9e0a3d0e244ba4f3abe4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=38ccb0abd0f754a7d3b95106cdccd54899a749be7833e49455eadf689941256c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ce086fb32bceed703e6f460a1c9835aaa421b83ee960d6dfee809d527b5e09;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-70.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80522afdd70276ee5ecab6e21fe3c0f9d8d1314ec31a717386aa86ec42d2fae4`  
		Last Modified: Tue, 25 Feb 2025 05:48:31 GMT  
		Size: 54.7 MB (54677020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443988cca47e542f6b4f11adb471ee7e46e5135c4faf5cb541eb2117c1437ebd`  
		Last Modified: Tue, 25 Feb 2025 05:48:29 GMT  
		Size: 1.5 MB (1488025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d165942b9cb195b39233afc43d6dcb9621a46665304b9b9a5900a21cc30690bb`  
		Last Modified: Tue, 25 Feb 2025 05:49:28 GMT  
		Size: 211.3 MB (211340533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0-70.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:034f29dc2cf4944be7d8f726c7403f0560bce7f58b9983022050200c0a47e753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f89f6050dbe4fc4c361f324b78a3cd07aac95e9126b3f81a7280745b40efc0`

```dockerfile
```

-	Layers:
	-	`sha256:91ee9049b0674a23a2a478dff3fd50d88be2d926ad75414699e78a1e5a89cfd9`  
		Last Modified: Tue, 25 Feb 2025 05:49:21 GMT  
		Size: 18.0 KB (18040 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8.0-70.1.beta-sdk`

```console
$ docker pull dart@sha256:6a3f40761c3fa74a597b4a6b077ae651cd87c02d1c15aa1aa6989030c5816095
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.8.0-70.1.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:dbff64306425ea6f7ab495b68c8073277fe885b1aff37f0655e4d51dfb9fe94e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296644093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adbeea1840fd94bc8fb1e1b1f9aa2abc3b62430ded33ae6c7bda5990a687b71f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c1b1d66c0fd37a432b268e43b06520b824ada88b268e9e0a3d0e244ba4f3abe4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=38ccb0abd0f754a7d3b95106cdccd54899a749be7833e49455eadf689941256c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ce086fb32bceed703e6f460a1c9835aaa421b83ee960d6dfee809d527b5e09;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-70.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd64cbcb2255822a221780af272c9d9f03b9d7f0e178f5f6f37e41e7532d6a4`  
		Last Modified: Tue, 25 Feb 2025 02:13:57 GMT  
		Size: 54.9 MB (54906703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbe373cbcef45e6a19683de9449a5262c7468d5918f0a8a3120cae60ca66598`  
		Last Modified: Tue, 25 Feb 2025 02:13:56 GMT  
		Size: 1.8 MB (1796911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ed192a04e915894a60de10e507c9ffaff9c360ccfc8f66efa78e48608a4696`  
		Last Modified: Tue, 25 Feb 2025 02:14:01 GMT  
		Size: 211.7 MB (211721146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0-70.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6bf2170c637ff046a22dac219dc0b4e9ea6b31281a9949d6f0fd9cc8dd143da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fd81d6a88a1f19640924a1e58b70b84cc799a0a1859b1cc94a42376c28d579`

```dockerfile
```

-	Layers:
	-	`sha256:2d3b87ba728f21d5219a8d61bba8f19039f8943261a7bb25e28e5aedb94e295e`  
		Last Modified: Tue, 25 Feb 2025 02:13:55 GMT  
		Size: 17.9 KB (17906 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.0-70.1.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:c031f2d72845f68e6558370848683261d9e75799af207c90bc41a0a62602f02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.3 MB (219315973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f787ee2dce46552a3e4edc390a8349514eff3dc6e772b6b9bebcdaf854ce6bc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c1b1d66c0fd37a432b268e43b06520b824ada88b268e9e0a3d0e244ba4f3abe4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=38ccb0abd0f754a7d3b95106cdccd54899a749be7833e49455eadf689941256c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ce086fb32bceed703e6f460a1c9835aaa421b83ee960d6dfee809d527b5e09;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-70.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5237f7e72c8f2131b9cde5d18f813ca79c323e6d50dcb0ee952dbf3febbdec40`  
		Last Modified: Tue, 25 Feb 2025 07:22:07 GMT  
		Size: 49.6 MB (49561814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0977386395adb5a5e238be6fc311e9c36206d68fd7d29b986b77d1ae9a968bbb`  
		Last Modified: Tue, 25 Feb 2025 07:22:05 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8291d9e33f2cacab92e8ac26e8a62fe150ce7178aed1445dc4d49aae993f18`  
		Last Modified: Tue, 25 Feb 2025 07:22:09 GMT  
		Size: 144.6 MB (144612718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0-70.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:3d855b21d7f2cc7261ceb05ed48ba9a132d4b7ae960750c272a967a1d414c97b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a76135a9102fdcb18cfbdc961b1514867f202bb32594480f423dbfd5240cdd`

```dockerfile
```

-	Layers:
	-	`sha256:77b17baa3d4085b12515992524200040bdd417c4a8531bed02b8e141e270083e`  
		Last Modified: Tue, 25 Feb 2025 07:22:05 GMT  
		Size: 18.0 KB (18008 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.0-70.1.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:7ec47a5bef9f97de020fd0bafa58712ecd96c1d28bfb6251650fc945c2010f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.6 MB (295554035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429d573a545a4dea83218d469bbfcd1c27de8963db715d742d0d60c8b3b187a0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c1b1d66c0fd37a432b268e43b06520b824ada88b268e9e0a3d0e244ba4f3abe4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=38ccb0abd0f754a7d3b95106cdccd54899a749be7833e49455eadf689941256c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ce086fb32bceed703e6f460a1c9835aaa421b83ee960d6dfee809d527b5e09;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-70.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80522afdd70276ee5ecab6e21fe3c0f9d8d1314ec31a717386aa86ec42d2fae4`  
		Last Modified: Tue, 25 Feb 2025 05:48:31 GMT  
		Size: 54.7 MB (54677020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443988cca47e542f6b4f11adb471ee7e46e5135c4faf5cb541eb2117c1437ebd`  
		Last Modified: Tue, 25 Feb 2025 05:48:29 GMT  
		Size: 1.5 MB (1488025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d165942b9cb195b39233afc43d6dcb9621a46665304b9b9a5900a21cc30690bb`  
		Last Modified: Tue, 25 Feb 2025 05:49:28 GMT  
		Size: 211.3 MB (211340533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0-70.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:034f29dc2cf4944be7d8f726c7403f0560bce7f58b9983022050200c0a47e753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f89f6050dbe4fc4c361f324b78a3cd07aac95e9126b3f81a7280745b40efc0`

```dockerfile
```

-	Layers:
	-	`sha256:91ee9049b0674a23a2a478dff3fd50d88be2d926ad75414699e78a1e5a89cfd9`  
		Last Modified: Tue, 25 Feb 2025 05:49:21 GMT  
		Size: 18.0 KB (18040 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:6a3f40761c3fa74a597b4a6b077ae651cd87c02d1c15aa1aa6989030c5816095
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
$ docker pull dart@sha256:dbff64306425ea6f7ab495b68c8073277fe885b1aff37f0655e4d51dfb9fe94e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296644093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adbeea1840fd94bc8fb1e1b1f9aa2abc3b62430ded33ae6c7bda5990a687b71f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c1b1d66c0fd37a432b268e43b06520b824ada88b268e9e0a3d0e244ba4f3abe4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=38ccb0abd0f754a7d3b95106cdccd54899a749be7833e49455eadf689941256c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ce086fb32bceed703e6f460a1c9835aaa421b83ee960d6dfee809d527b5e09;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-70.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd64cbcb2255822a221780af272c9d9f03b9d7f0e178f5f6f37e41e7532d6a4`  
		Last Modified: Tue, 25 Feb 2025 02:13:57 GMT  
		Size: 54.9 MB (54906703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbe373cbcef45e6a19683de9449a5262c7468d5918f0a8a3120cae60ca66598`  
		Last Modified: Tue, 25 Feb 2025 02:13:56 GMT  
		Size: 1.8 MB (1796911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ed192a04e915894a60de10e507c9ffaff9c360ccfc8f66efa78e48608a4696`  
		Last Modified: Tue, 25 Feb 2025 02:14:01 GMT  
		Size: 211.7 MB (211721146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:6bf2170c637ff046a22dac219dc0b4e9ea6b31281a9949d6f0fd9cc8dd143da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fd81d6a88a1f19640924a1e58b70b84cc799a0a1859b1cc94a42376c28d579`

```dockerfile
```

-	Layers:
	-	`sha256:2d3b87ba728f21d5219a8d61bba8f19039f8943261a7bb25e28e5aedb94e295e`  
		Last Modified: Tue, 25 Feb 2025 02:13:55 GMT  
		Size: 17.9 KB (17906 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:c031f2d72845f68e6558370848683261d9e75799af207c90bc41a0a62602f02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.3 MB (219315973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f787ee2dce46552a3e4edc390a8349514eff3dc6e772b6b9bebcdaf854ce6bc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c1b1d66c0fd37a432b268e43b06520b824ada88b268e9e0a3d0e244ba4f3abe4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=38ccb0abd0f754a7d3b95106cdccd54899a749be7833e49455eadf689941256c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ce086fb32bceed703e6f460a1c9835aaa421b83ee960d6dfee809d527b5e09;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-70.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5237f7e72c8f2131b9cde5d18f813ca79c323e6d50dcb0ee952dbf3febbdec40`  
		Last Modified: Tue, 25 Feb 2025 07:22:07 GMT  
		Size: 49.6 MB (49561814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0977386395adb5a5e238be6fc311e9c36206d68fd7d29b986b77d1ae9a968bbb`  
		Last Modified: Tue, 25 Feb 2025 07:22:05 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8291d9e33f2cacab92e8ac26e8a62fe150ce7178aed1445dc4d49aae993f18`  
		Last Modified: Tue, 25 Feb 2025 07:22:09 GMT  
		Size: 144.6 MB (144612718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:3d855b21d7f2cc7261ceb05ed48ba9a132d4b7ae960750c272a967a1d414c97b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a76135a9102fdcb18cfbdc961b1514867f202bb32594480f423dbfd5240cdd`

```dockerfile
```

-	Layers:
	-	`sha256:77b17baa3d4085b12515992524200040bdd417c4a8531bed02b8e141e270083e`  
		Last Modified: Tue, 25 Feb 2025 07:22:05 GMT  
		Size: 18.0 KB (18008 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:7ec47a5bef9f97de020fd0bafa58712ecd96c1d28bfb6251650fc945c2010f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.6 MB (295554035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429d573a545a4dea83218d469bbfcd1c27de8963db715d742d0d60c8b3b187a0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c1b1d66c0fd37a432b268e43b06520b824ada88b268e9e0a3d0e244ba4f3abe4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=38ccb0abd0f754a7d3b95106cdccd54899a749be7833e49455eadf689941256c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ce086fb32bceed703e6f460a1c9835aaa421b83ee960d6dfee809d527b5e09;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-70.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80522afdd70276ee5ecab6e21fe3c0f9d8d1314ec31a717386aa86ec42d2fae4`  
		Last Modified: Tue, 25 Feb 2025 05:48:31 GMT  
		Size: 54.7 MB (54677020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443988cca47e542f6b4f11adb471ee7e46e5135c4faf5cb541eb2117c1437ebd`  
		Last Modified: Tue, 25 Feb 2025 05:48:29 GMT  
		Size: 1.5 MB (1488025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d165942b9cb195b39233afc43d6dcb9621a46665304b9b9a5900a21cc30690bb`  
		Last Modified: Tue, 25 Feb 2025 05:49:28 GMT  
		Size: 211.3 MB (211340533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:034f29dc2cf4944be7d8f726c7403f0560bce7f58b9983022050200c0a47e753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f89f6050dbe4fc4c361f324b78a3cd07aac95e9126b3f81a7280745b40efc0`

```dockerfile
```

-	Layers:
	-	`sha256:91ee9049b0674a23a2a478dff3fd50d88be2d926ad75414699e78a1e5a89cfd9`  
		Last Modified: Tue, 25 Feb 2025 05:49:21 GMT  
		Size: 18.0 KB (18040 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:6a3f40761c3fa74a597b4a6b077ae651cd87c02d1c15aa1aa6989030c5816095
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
$ docker pull dart@sha256:dbff64306425ea6f7ab495b68c8073277fe885b1aff37f0655e4d51dfb9fe94e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296644093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adbeea1840fd94bc8fb1e1b1f9aa2abc3b62430ded33ae6c7bda5990a687b71f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c1b1d66c0fd37a432b268e43b06520b824ada88b268e9e0a3d0e244ba4f3abe4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=38ccb0abd0f754a7d3b95106cdccd54899a749be7833e49455eadf689941256c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ce086fb32bceed703e6f460a1c9835aaa421b83ee960d6dfee809d527b5e09;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-70.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd64cbcb2255822a221780af272c9d9f03b9d7f0e178f5f6f37e41e7532d6a4`  
		Last Modified: Tue, 25 Feb 2025 02:13:57 GMT  
		Size: 54.9 MB (54906703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbe373cbcef45e6a19683de9449a5262c7468d5918f0a8a3120cae60ca66598`  
		Last Modified: Tue, 25 Feb 2025 02:13:56 GMT  
		Size: 1.8 MB (1796911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ed192a04e915894a60de10e507c9ffaff9c360ccfc8f66efa78e48608a4696`  
		Last Modified: Tue, 25 Feb 2025 02:14:01 GMT  
		Size: 211.7 MB (211721146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6bf2170c637ff046a22dac219dc0b4e9ea6b31281a9949d6f0fd9cc8dd143da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fd81d6a88a1f19640924a1e58b70b84cc799a0a1859b1cc94a42376c28d579`

```dockerfile
```

-	Layers:
	-	`sha256:2d3b87ba728f21d5219a8d61bba8f19039f8943261a7bb25e28e5aedb94e295e`  
		Last Modified: Tue, 25 Feb 2025 02:13:55 GMT  
		Size: 17.9 KB (17906 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:c031f2d72845f68e6558370848683261d9e75799af207c90bc41a0a62602f02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.3 MB (219315973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f787ee2dce46552a3e4edc390a8349514eff3dc6e772b6b9bebcdaf854ce6bc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c1b1d66c0fd37a432b268e43b06520b824ada88b268e9e0a3d0e244ba4f3abe4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=38ccb0abd0f754a7d3b95106cdccd54899a749be7833e49455eadf689941256c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ce086fb32bceed703e6f460a1c9835aaa421b83ee960d6dfee809d527b5e09;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-70.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5237f7e72c8f2131b9cde5d18f813ca79c323e6d50dcb0ee952dbf3febbdec40`  
		Last Modified: Tue, 25 Feb 2025 07:22:07 GMT  
		Size: 49.6 MB (49561814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0977386395adb5a5e238be6fc311e9c36206d68fd7d29b986b77d1ae9a968bbb`  
		Last Modified: Tue, 25 Feb 2025 07:22:05 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8291d9e33f2cacab92e8ac26e8a62fe150ce7178aed1445dc4d49aae993f18`  
		Last Modified: Tue, 25 Feb 2025 07:22:09 GMT  
		Size: 144.6 MB (144612718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:3d855b21d7f2cc7261ceb05ed48ba9a132d4b7ae960750c272a967a1d414c97b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a76135a9102fdcb18cfbdc961b1514867f202bb32594480f423dbfd5240cdd`

```dockerfile
```

-	Layers:
	-	`sha256:77b17baa3d4085b12515992524200040bdd417c4a8531bed02b8e141e270083e`  
		Last Modified: Tue, 25 Feb 2025 07:22:05 GMT  
		Size: 18.0 KB (18008 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:7ec47a5bef9f97de020fd0bafa58712ecd96c1d28bfb6251650fc945c2010f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.6 MB (295554035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429d573a545a4dea83218d469bbfcd1c27de8963db715d742d0d60c8b3b187a0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c1b1d66c0fd37a432b268e43b06520b824ada88b268e9e0a3d0e244ba4f3abe4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=38ccb0abd0f754a7d3b95106cdccd54899a749be7833e49455eadf689941256c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ce086fb32bceed703e6f460a1c9835aaa421b83ee960d6dfee809d527b5e09;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-70.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80522afdd70276ee5ecab6e21fe3c0f9d8d1314ec31a717386aa86ec42d2fae4`  
		Last Modified: Tue, 25 Feb 2025 05:48:31 GMT  
		Size: 54.7 MB (54677020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443988cca47e542f6b4f11adb471ee7e46e5135c4faf5cb541eb2117c1437ebd`  
		Last Modified: Tue, 25 Feb 2025 05:48:29 GMT  
		Size: 1.5 MB (1488025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d165942b9cb195b39233afc43d6dcb9621a46665304b9b9a5900a21cc30690bb`  
		Last Modified: Tue, 25 Feb 2025 05:49:28 GMT  
		Size: 211.3 MB (211340533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:034f29dc2cf4944be7d8f726c7403f0560bce7f58b9983022050200c0a47e753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f89f6050dbe4fc4c361f324b78a3cd07aac95e9126b3f81a7280745b40efc0`

```dockerfile
```

-	Layers:
	-	`sha256:91ee9049b0674a23a2a478dff3fd50d88be2d926ad75414699e78a1e5a89cfd9`  
		Last Modified: Tue, 25 Feb 2025 05:49:21 GMT  
		Size: 18.0 KB (18040 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:9fb41fc1eefdf432694e17b0f80c9135b1f79dd3f645c403f98ed5ae71799c36
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
$ docker pull dart@sha256:b43c3f563f15dddf5e962075c1faddfebe1a094b6144718e65a1706cb5b28951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304966717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb5db526fd50d343e0012bb9386d775dd776a8eda76e18672ead7a5a7f5cabb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c7a891ed4d4ce462192c75f6acfaaa58a1da6eb029e83aa11eb66544552f7c`  
		Last Modified: Tue, 25 Feb 2025 03:22:22 GMT  
		Size: 54.9 MB (54906829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774f8223e39d93a20bddd53031475c142c44e17195a7f12b6c598e2db7e9907a`  
		Last Modified: Tue, 25 Feb 2025 03:22:20 GMT  
		Size: 1.8 MB (1796915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d1765a8b4993ff038f8e0c1b88d3cbb5ed04d215a238ae34a65c855a1a33a7`  
		Last Modified: Tue, 25 Feb 2025 03:22:26 GMT  
		Size: 220.0 MB (220043640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:169df6ff0e0981d81b3bb4d11e57b6a80b53331b023269151337081683e46041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8cb0ea4652d056835eef3e5f7dfc152ec0d53e1c802bbc00f28938bf765cc60`

```dockerfile
```

-	Layers:
	-	`sha256:7d677a1352e3e2dd50ea7d03c7b98fdfab0a02c53b7b95e3a2330691360aea1e`  
		Last Modified: Tue, 25 Feb 2025 03:22:20 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:febe29a2dbb15f1af5716b8e31db5df7726b12d0e05688bb64e305eba8627f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226300684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747b24a70e7d9017ee70e379389b8ee87f7c8595ae17649befdce5d789459b88`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5237f7e72c8f2131b9cde5d18f813ca79c323e6d50dcb0ee952dbf3febbdec40`  
		Last Modified: Tue, 25 Feb 2025 07:22:07 GMT  
		Size: 49.6 MB (49561814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0977386395adb5a5e238be6fc311e9c36206d68fd7d29b986b77d1ae9a968bbb`  
		Last Modified: Tue, 25 Feb 2025 07:22:05 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3b45e78f7fe8dc51f123bb726524bd6c8d6e5245ad42836bd0fd1b3b5b2b26`  
		Last Modified: Tue, 25 Feb 2025 13:41:48 GMT  
		Size: 151.6 MB (151597429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:1af9585a83934e03ab0677a55db0ed0922fd0c0baecccf06d373d6b08743fe1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4370e355c021d94d848ea7dea1197e02c234163c22c087eeb771b2ad7efe4570`

```dockerfile
```

-	Layers:
	-	`sha256:beea83ecd2bbc9359497d0fb39ca7a8adf3af6bfe66b08574f61581607b228a9`  
		Last Modified: Tue, 25 Feb 2025 13:41:44 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:9cf616067bcbd55ae946d8f559b0ce971cf8773aa95de21187ee844f1317e05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303823647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ae015985756d0b209352bb079df8905fb1b3f933e07ed72266c8d95f9cb226`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80522afdd70276ee5ecab6e21fe3c0f9d8d1314ec31a717386aa86ec42d2fae4`  
		Last Modified: Tue, 25 Feb 2025 05:48:31 GMT  
		Size: 54.7 MB (54677020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443988cca47e542f6b4f11adb471ee7e46e5135c4faf5cb541eb2117c1437ebd`  
		Last Modified: Tue, 25 Feb 2025 05:48:29 GMT  
		Size: 1.5 MB (1488025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790f1ce84f87eace2e2834f6fb45d00c3c0da18abb45fe361e7919ef6d3f703e`  
		Last Modified: Tue, 25 Feb 2025 05:48:36 GMT  
		Size: 219.6 MB (219610145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:29102ee6a46ac1024761115e544098a021cc3632a3ba2d23bfaf1b92b8e4d133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5ed1c6b1c90f53adfed73e2e5398a7228564b1e89332dfcb8cf983337b89b6`

```dockerfile
```

-	Layers:
	-	`sha256:0d5bd9b1b0abac9c7743438d0f786399f3555ccd6b5a945f2e5f043b789d87cf`  
		Last Modified: Tue, 25 Feb 2025 05:48:29 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:9fb41fc1eefdf432694e17b0f80c9135b1f79dd3f645c403f98ed5ae71799c36
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
$ docker pull dart@sha256:b43c3f563f15dddf5e962075c1faddfebe1a094b6144718e65a1706cb5b28951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304966717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb5db526fd50d343e0012bb9386d775dd776a8eda76e18672ead7a5a7f5cabb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c7a891ed4d4ce462192c75f6acfaaa58a1da6eb029e83aa11eb66544552f7c`  
		Last Modified: Tue, 25 Feb 2025 03:22:22 GMT  
		Size: 54.9 MB (54906829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774f8223e39d93a20bddd53031475c142c44e17195a7f12b6c598e2db7e9907a`  
		Last Modified: Tue, 25 Feb 2025 03:22:20 GMT  
		Size: 1.8 MB (1796915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d1765a8b4993ff038f8e0c1b88d3cbb5ed04d215a238ae34a65c855a1a33a7`  
		Last Modified: Tue, 25 Feb 2025 03:22:26 GMT  
		Size: 220.0 MB (220043640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:169df6ff0e0981d81b3bb4d11e57b6a80b53331b023269151337081683e46041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8cb0ea4652d056835eef3e5f7dfc152ec0d53e1c802bbc00f28938bf765cc60`

```dockerfile
```

-	Layers:
	-	`sha256:7d677a1352e3e2dd50ea7d03c7b98fdfab0a02c53b7b95e3a2330691360aea1e`  
		Last Modified: Tue, 25 Feb 2025 03:22:20 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:febe29a2dbb15f1af5716b8e31db5df7726b12d0e05688bb64e305eba8627f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226300684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747b24a70e7d9017ee70e379389b8ee87f7c8595ae17649befdce5d789459b88`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5237f7e72c8f2131b9cde5d18f813ca79c323e6d50dcb0ee952dbf3febbdec40`  
		Last Modified: Tue, 25 Feb 2025 07:22:07 GMT  
		Size: 49.6 MB (49561814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0977386395adb5a5e238be6fc311e9c36206d68fd7d29b986b77d1ae9a968bbb`  
		Last Modified: Tue, 25 Feb 2025 07:22:05 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3b45e78f7fe8dc51f123bb726524bd6c8d6e5245ad42836bd0fd1b3b5b2b26`  
		Last Modified: Tue, 25 Feb 2025 13:41:48 GMT  
		Size: 151.6 MB (151597429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1af9585a83934e03ab0677a55db0ed0922fd0c0baecccf06d373d6b08743fe1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4370e355c021d94d848ea7dea1197e02c234163c22c087eeb771b2ad7efe4570`

```dockerfile
```

-	Layers:
	-	`sha256:beea83ecd2bbc9359497d0fb39ca7a8adf3af6bfe66b08574f61581607b228a9`  
		Last Modified: Tue, 25 Feb 2025 13:41:44 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:9cf616067bcbd55ae946d8f559b0ce971cf8773aa95de21187ee844f1317e05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303823647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ae015985756d0b209352bb079df8905fb1b3f933e07ed72266c8d95f9cb226`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80522afdd70276ee5ecab6e21fe3c0f9d8d1314ec31a717386aa86ec42d2fae4`  
		Last Modified: Tue, 25 Feb 2025 05:48:31 GMT  
		Size: 54.7 MB (54677020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443988cca47e542f6b4f11adb471ee7e46e5135c4faf5cb541eb2117c1437ebd`  
		Last Modified: Tue, 25 Feb 2025 05:48:29 GMT  
		Size: 1.5 MB (1488025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790f1ce84f87eace2e2834f6fb45d00c3c0da18abb45fe361e7919ef6d3f703e`  
		Last Modified: Tue, 25 Feb 2025 05:48:36 GMT  
		Size: 219.6 MB (219610145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:29102ee6a46ac1024761115e544098a021cc3632a3ba2d23bfaf1b92b8e4d133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5ed1c6b1c90f53adfed73e2e5398a7228564b1e89332dfcb8cf983337b89b6`

```dockerfile
```

-	Layers:
	-	`sha256:0d5bd9b1b0abac9c7743438d0f786399f3555ccd6b5a945f2e5f043b789d87cf`  
		Last Modified: Tue, 25 Feb 2025 05:48:29 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:9fb41fc1eefdf432694e17b0f80c9135b1f79dd3f645c403f98ed5ae71799c36
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
$ docker pull dart@sha256:b43c3f563f15dddf5e962075c1faddfebe1a094b6144718e65a1706cb5b28951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304966717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb5db526fd50d343e0012bb9386d775dd776a8eda76e18672ead7a5a7f5cabb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c7a891ed4d4ce462192c75f6acfaaa58a1da6eb029e83aa11eb66544552f7c`  
		Last Modified: Tue, 25 Feb 2025 03:22:22 GMT  
		Size: 54.9 MB (54906829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774f8223e39d93a20bddd53031475c142c44e17195a7f12b6c598e2db7e9907a`  
		Last Modified: Tue, 25 Feb 2025 03:22:20 GMT  
		Size: 1.8 MB (1796915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d1765a8b4993ff038f8e0c1b88d3cbb5ed04d215a238ae34a65c855a1a33a7`  
		Last Modified: Tue, 25 Feb 2025 03:22:26 GMT  
		Size: 220.0 MB (220043640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:169df6ff0e0981d81b3bb4d11e57b6a80b53331b023269151337081683e46041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8cb0ea4652d056835eef3e5f7dfc152ec0d53e1c802bbc00f28938bf765cc60`

```dockerfile
```

-	Layers:
	-	`sha256:7d677a1352e3e2dd50ea7d03c7b98fdfab0a02c53b7b95e3a2330691360aea1e`  
		Last Modified: Tue, 25 Feb 2025 03:22:20 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:febe29a2dbb15f1af5716b8e31db5df7726b12d0e05688bb64e305eba8627f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226300684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747b24a70e7d9017ee70e379389b8ee87f7c8595ae17649befdce5d789459b88`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5237f7e72c8f2131b9cde5d18f813ca79c323e6d50dcb0ee952dbf3febbdec40`  
		Last Modified: Tue, 25 Feb 2025 07:22:07 GMT  
		Size: 49.6 MB (49561814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0977386395adb5a5e238be6fc311e9c36206d68fd7d29b986b77d1ae9a968bbb`  
		Last Modified: Tue, 25 Feb 2025 07:22:05 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3b45e78f7fe8dc51f123bb726524bd6c8d6e5245ad42836bd0fd1b3b5b2b26`  
		Last Modified: Tue, 25 Feb 2025 13:41:48 GMT  
		Size: 151.6 MB (151597429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:1af9585a83934e03ab0677a55db0ed0922fd0c0baecccf06d373d6b08743fe1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4370e355c021d94d848ea7dea1197e02c234163c22c087eeb771b2ad7efe4570`

```dockerfile
```

-	Layers:
	-	`sha256:beea83ecd2bbc9359497d0fb39ca7a8adf3af6bfe66b08574f61581607b228a9`  
		Last Modified: Tue, 25 Feb 2025 13:41:44 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:9cf616067bcbd55ae946d8f559b0ce971cf8773aa95de21187ee844f1317e05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303823647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ae015985756d0b209352bb079df8905fb1b3f933e07ed72266c8d95f9cb226`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80522afdd70276ee5ecab6e21fe3c0f9d8d1314ec31a717386aa86ec42d2fae4`  
		Last Modified: Tue, 25 Feb 2025 05:48:31 GMT  
		Size: 54.7 MB (54677020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443988cca47e542f6b4f11adb471ee7e46e5135c4faf5cb541eb2117c1437ebd`  
		Last Modified: Tue, 25 Feb 2025 05:48:29 GMT  
		Size: 1.5 MB (1488025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790f1ce84f87eace2e2834f6fb45d00c3c0da18abb45fe361e7919ef6d3f703e`  
		Last Modified: Tue, 25 Feb 2025 05:48:36 GMT  
		Size: 219.6 MB (219610145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:29102ee6a46ac1024761115e544098a021cc3632a3ba2d23bfaf1b92b8e4d133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5ed1c6b1c90f53adfed73e2e5398a7228564b1e89332dfcb8cf983337b89b6`

```dockerfile
```

-	Layers:
	-	`sha256:0d5bd9b1b0abac9c7743438d0f786399f3555ccd6b5a945f2e5f043b789d87cf`  
		Last Modified: Tue, 25 Feb 2025 05:48:29 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:9fb41fc1eefdf432694e17b0f80c9135b1f79dd3f645c403f98ed5ae71799c36
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
$ docker pull dart@sha256:b43c3f563f15dddf5e962075c1faddfebe1a094b6144718e65a1706cb5b28951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304966717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb5db526fd50d343e0012bb9386d775dd776a8eda76e18672ead7a5a7f5cabb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c7a891ed4d4ce462192c75f6acfaaa58a1da6eb029e83aa11eb66544552f7c`  
		Last Modified: Tue, 25 Feb 2025 03:22:22 GMT  
		Size: 54.9 MB (54906829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774f8223e39d93a20bddd53031475c142c44e17195a7f12b6c598e2db7e9907a`  
		Last Modified: Tue, 25 Feb 2025 03:22:20 GMT  
		Size: 1.8 MB (1796915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d1765a8b4993ff038f8e0c1b88d3cbb5ed04d215a238ae34a65c855a1a33a7`  
		Last Modified: Tue, 25 Feb 2025 03:22:26 GMT  
		Size: 220.0 MB (220043640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:169df6ff0e0981d81b3bb4d11e57b6a80b53331b023269151337081683e46041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8cb0ea4652d056835eef3e5f7dfc152ec0d53e1c802bbc00f28938bf765cc60`

```dockerfile
```

-	Layers:
	-	`sha256:7d677a1352e3e2dd50ea7d03c7b98fdfab0a02c53b7b95e3a2330691360aea1e`  
		Last Modified: Tue, 25 Feb 2025 03:22:20 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:febe29a2dbb15f1af5716b8e31db5df7726b12d0e05688bb64e305eba8627f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226300684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747b24a70e7d9017ee70e379389b8ee87f7c8595ae17649befdce5d789459b88`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5237f7e72c8f2131b9cde5d18f813ca79c323e6d50dcb0ee952dbf3febbdec40`  
		Last Modified: Tue, 25 Feb 2025 07:22:07 GMT  
		Size: 49.6 MB (49561814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0977386395adb5a5e238be6fc311e9c36206d68fd7d29b986b77d1ae9a968bbb`  
		Last Modified: Tue, 25 Feb 2025 07:22:05 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3b45e78f7fe8dc51f123bb726524bd6c8d6e5245ad42836bd0fd1b3b5b2b26`  
		Last Modified: Tue, 25 Feb 2025 13:41:48 GMT  
		Size: 151.6 MB (151597429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1af9585a83934e03ab0677a55db0ed0922fd0c0baecccf06d373d6b08743fe1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4370e355c021d94d848ea7dea1197e02c234163c22c087eeb771b2ad7efe4570`

```dockerfile
```

-	Layers:
	-	`sha256:beea83ecd2bbc9359497d0fb39ca7a8adf3af6bfe66b08574f61581607b228a9`  
		Last Modified: Tue, 25 Feb 2025 13:41:44 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:9cf616067bcbd55ae946d8f559b0ce971cf8773aa95de21187ee844f1317e05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303823647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ae015985756d0b209352bb079df8905fb1b3f933e07ed72266c8d95f9cb226`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Feb 2025 08:49:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80522afdd70276ee5ecab6e21fe3c0f9d8d1314ec31a717386aa86ec42d2fae4`  
		Last Modified: Tue, 25 Feb 2025 05:48:31 GMT  
		Size: 54.7 MB (54677020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443988cca47e542f6b4f11adb471ee7e46e5135c4faf5cb541eb2117c1437ebd`  
		Last Modified: Tue, 25 Feb 2025 05:48:29 GMT  
		Size: 1.5 MB (1488025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790f1ce84f87eace2e2834f6fb45d00c3c0da18abb45fe361e7919ef6d3f703e`  
		Last Modified: Tue, 25 Feb 2025 05:48:36 GMT  
		Size: 219.6 MB (219610145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:29102ee6a46ac1024761115e544098a021cc3632a3ba2d23bfaf1b92b8e4d133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5ed1c6b1c90f53adfed73e2e5398a7228564b1e89332dfcb8cf983337b89b6`

```dockerfile
```

-	Layers:
	-	`sha256:0d5bd9b1b0abac9c7743438d0f786399f3555ccd6b5a945f2e5f043b789d87cf`  
		Last Modified: Tue, 25 Feb 2025 05:48:29 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json
