<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.7`](#dart37)
-	[`dart:3.7-sdk`](#dart37-sdk)
-	[`dart:3.7.1`](#dart371)
-	[`dart:3.7.1-sdk`](#dart371-sdk)
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
$ docker pull dart@sha256:5d40556368d94af9a1b41447cf1e5635dec18dc3f52c66096e1561be6580a321
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
$ docker pull dart@sha256:8d3825a508394f0e9eaabb81e9eff8d52fcb23f55c842d08a648ee254d3879a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304930725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c9c9268d1361e6c26ef3dd09475bd80909fb46f07afe944beadd783107c101`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8f516bb78ef3ba2aaba44acb0935922bd5c8b107ee9eaba02150613734eaf9`  
		Last Modified: Wed, 26 Feb 2025 22:30:22 GMT  
		Size: 54.9 MB (54906797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aae2eb44aadb93c85b847cba6f77a5f4ccc2d100468e1f2fb2f63602840f5c`  
		Last Modified: Wed, 26 Feb 2025 22:30:20 GMT  
		Size: 1.8 MB (1796912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66854d8af3d8fdaf583800167c14ed49972798b625ccb8622ee8bea3d264a78`  
		Last Modified: Wed, 26 Feb 2025 22:30:26 GMT  
		Size: 220.0 MB (220007683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:ddc154eddd84bf7937ae0eaab0fec5427fbfe56479440b9b513dc8bdf2168247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21231a7ac629ef3212c7d6adfc4cd2154f9375abd8688c9958f12e4fbdd0a40e`

```dockerfile
```

-	Layers:
	-	`sha256:45ce83ec221425122a41bacb4fdbb7139cf2c6ae9c0f9f585818c4c48ad44c2e`  
		Last Modified: Wed, 26 Feb 2025 22:30:20 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:a7567cde4ecc1ffea3e6418dab3d8f63dcbeadd0f77edb7dfe1a3f9fef375683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226295824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f45f579fbcd6f82488a20ef3cea4b92d9090a74b9583665ed2e0179c850c41`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a359f18382a9bcd45ac7a3c553332cd0869d70af84eecf35d256ad8e43693e`  
		Last Modified: Wed, 26 Feb 2025 22:30:54 GMT  
		Size: 49.6 MB (49561776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5175bf9db12ef7e7e9057eb5a889211ad5a0307eff0d459e22a21a7cffa3c33e`  
		Last Modified: Wed, 26 Feb 2025 22:30:53 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf06b0e14fb02b9d2b31bdf62ce720061b537522d8991850f51dcc8f47519874`  
		Last Modified: Wed, 26 Feb 2025 22:30:56 GMT  
		Size: 151.6 MB (151592607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:e620675e509085d8c37353d4db6e3f3372d75d2c4f0596c0645c74aee686ecfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd7aedd8f4ef8ae28889e348df03e3d2961d4bcbe9b81f2edb92e6492d6d798`

```dockerfile
```

-	Layers:
	-	`sha256:6a91f3dbee63f59c739a877245c060505be61b4f23c1e73f4eb779f06d25ea43`  
		Last Modified: Wed, 26 Feb 2025 22:30:52 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3e69ad67d62bcf313d3f0d97ecf562c4bf5310aebc04819f5ba144174c995d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303839605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b8227a1a7b249a87483cddb9616bb5ae4ff122c1fd847884084a0e48340eb3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e79ef03a42dbe2876898f16a38c0286273d341eed88ff0c63ea5125c37c702e`  
		Last Modified: Wed, 26 Feb 2025 22:30:26 GMT  
		Size: 54.7 MB (54677213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff505137b20bd757addb3d29c71d8e254b1caea248ea9266e29c104824341c22`  
		Last Modified: Wed, 26 Feb 2025 22:30:24 GMT  
		Size: 1.5 MB (1488027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb529a1ffd698d3aa55bb2808f18abd18837ea54fc32158d29613fb3f1e0f6d7`  
		Last Modified: Wed, 26 Feb 2025 22:30:30 GMT  
		Size: 219.6 MB (219625908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:3991581d9bce6f45923638ff2548ff0c00e286acf0b87e0bddacdcb98fbeb64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ecd3f2c7f552541823962446115ae4723ea78ef00f4264043845dc4e12c370`

```dockerfile
```

-	Layers:
	-	`sha256:d2ab17a330033f2f7ee682e526d90b897f88c863e78575ef2b4efe6cce6eaf95`  
		Last Modified: Wed, 26 Feb 2025 22:30:24 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:5d40556368d94af9a1b41447cf1e5635dec18dc3f52c66096e1561be6580a321
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
$ docker pull dart@sha256:8d3825a508394f0e9eaabb81e9eff8d52fcb23f55c842d08a648ee254d3879a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304930725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c9c9268d1361e6c26ef3dd09475bd80909fb46f07afe944beadd783107c101`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8f516bb78ef3ba2aaba44acb0935922bd5c8b107ee9eaba02150613734eaf9`  
		Last Modified: Wed, 26 Feb 2025 22:30:22 GMT  
		Size: 54.9 MB (54906797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aae2eb44aadb93c85b847cba6f77a5f4ccc2d100468e1f2fb2f63602840f5c`  
		Last Modified: Wed, 26 Feb 2025 22:30:20 GMT  
		Size: 1.8 MB (1796912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66854d8af3d8fdaf583800167c14ed49972798b625ccb8622ee8bea3d264a78`  
		Last Modified: Wed, 26 Feb 2025 22:30:26 GMT  
		Size: 220.0 MB (220007683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ddc154eddd84bf7937ae0eaab0fec5427fbfe56479440b9b513dc8bdf2168247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21231a7ac629ef3212c7d6adfc4cd2154f9375abd8688c9958f12e4fbdd0a40e`

```dockerfile
```

-	Layers:
	-	`sha256:45ce83ec221425122a41bacb4fdbb7139cf2c6ae9c0f9f585818c4c48ad44c2e`  
		Last Modified: Wed, 26 Feb 2025 22:30:20 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:a7567cde4ecc1ffea3e6418dab3d8f63dcbeadd0f77edb7dfe1a3f9fef375683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226295824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f45f579fbcd6f82488a20ef3cea4b92d9090a74b9583665ed2e0179c850c41`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a359f18382a9bcd45ac7a3c553332cd0869d70af84eecf35d256ad8e43693e`  
		Last Modified: Wed, 26 Feb 2025 22:30:54 GMT  
		Size: 49.6 MB (49561776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5175bf9db12ef7e7e9057eb5a889211ad5a0307eff0d459e22a21a7cffa3c33e`  
		Last Modified: Wed, 26 Feb 2025 22:30:53 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf06b0e14fb02b9d2b31bdf62ce720061b537522d8991850f51dcc8f47519874`  
		Last Modified: Wed, 26 Feb 2025 22:30:56 GMT  
		Size: 151.6 MB (151592607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e620675e509085d8c37353d4db6e3f3372d75d2c4f0596c0645c74aee686ecfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd7aedd8f4ef8ae28889e348df03e3d2961d4bcbe9b81f2edb92e6492d6d798`

```dockerfile
```

-	Layers:
	-	`sha256:6a91f3dbee63f59c739a877245c060505be61b4f23c1e73f4eb779f06d25ea43`  
		Last Modified: Wed, 26 Feb 2025 22:30:52 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3e69ad67d62bcf313d3f0d97ecf562c4bf5310aebc04819f5ba144174c995d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303839605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b8227a1a7b249a87483cddb9616bb5ae4ff122c1fd847884084a0e48340eb3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e79ef03a42dbe2876898f16a38c0286273d341eed88ff0c63ea5125c37c702e`  
		Last Modified: Wed, 26 Feb 2025 22:30:26 GMT  
		Size: 54.7 MB (54677213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff505137b20bd757addb3d29c71d8e254b1caea248ea9266e29c104824341c22`  
		Last Modified: Wed, 26 Feb 2025 22:30:24 GMT  
		Size: 1.5 MB (1488027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb529a1ffd698d3aa55bb2808f18abd18837ea54fc32158d29613fb3f1e0f6d7`  
		Last Modified: Wed, 26 Feb 2025 22:30:30 GMT  
		Size: 219.6 MB (219625908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:3991581d9bce6f45923638ff2548ff0c00e286acf0b87e0bddacdcb98fbeb64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ecd3f2c7f552541823962446115ae4723ea78ef00f4264043845dc4e12c370`

```dockerfile
```

-	Layers:
	-	`sha256:d2ab17a330033f2f7ee682e526d90b897f88c863e78575ef2b4efe6cce6eaf95`  
		Last Modified: Wed, 26 Feb 2025 22:30:24 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.7`

```console
$ docker pull dart@sha256:5d40556368d94af9a1b41447cf1e5635dec18dc3f52c66096e1561be6580a321
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
$ docker pull dart@sha256:8d3825a508394f0e9eaabb81e9eff8d52fcb23f55c842d08a648ee254d3879a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304930725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c9c9268d1361e6c26ef3dd09475bd80909fb46f07afe944beadd783107c101`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8f516bb78ef3ba2aaba44acb0935922bd5c8b107ee9eaba02150613734eaf9`  
		Last Modified: Wed, 26 Feb 2025 22:30:22 GMT  
		Size: 54.9 MB (54906797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aae2eb44aadb93c85b847cba6f77a5f4ccc2d100468e1f2fb2f63602840f5c`  
		Last Modified: Wed, 26 Feb 2025 22:30:20 GMT  
		Size: 1.8 MB (1796912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66854d8af3d8fdaf583800167c14ed49972798b625ccb8622ee8bea3d264a78`  
		Last Modified: Wed, 26 Feb 2025 22:30:26 GMT  
		Size: 220.0 MB (220007683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7` - unknown; unknown

```console
$ docker pull dart@sha256:ddc154eddd84bf7937ae0eaab0fec5427fbfe56479440b9b513dc8bdf2168247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21231a7ac629ef3212c7d6adfc4cd2154f9375abd8688c9958f12e4fbdd0a40e`

```dockerfile
```

-	Layers:
	-	`sha256:45ce83ec221425122a41bacb4fdbb7139cf2c6ae9c0f9f585818c4c48ad44c2e`  
		Last Modified: Wed, 26 Feb 2025 22:30:20 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7` - linux; arm variant v7

```console
$ docker pull dart@sha256:a7567cde4ecc1ffea3e6418dab3d8f63dcbeadd0f77edb7dfe1a3f9fef375683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226295824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f45f579fbcd6f82488a20ef3cea4b92d9090a74b9583665ed2e0179c850c41`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a359f18382a9bcd45ac7a3c553332cd0869d70af84eecf35d256ad8e43693e`  
		Last Modified: Wed, 26 Feb 2025 22:30:54 GMT  
		Size: 49.6 MB (49561776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5175bf9db12ef7e7e9057eb5a889211ad5a0307eff0d459e22a21a7cffa3c33e`  
		Last Modified: Wed, 26 Feb 2025 22:30:53 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf06b0e14fb02b9d2b31bdf62ce720061b537522d8991850f51dcc8f47519874`  
		Last Modified: Wed, 26 Feb 2025 22:30:56 GMT  
		Size: 151.6 MB (151592607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7` - unknown; unknown

```console
$ docker pull dart@sha256:e620675e509085d8c37353d4db6e3f3372d75d2c4f0596c0645c74aee686ecfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd7aedd8f4ef8ae28889e348df03e3d2961d4bcbe9b81f2edb92e6492d6d798`

```dockerfile
```

-	Layers:
	-	`sha256:6a91f3dbee63f59c739a877245c060505be61b4f23c1e73f4eb779f06d25ea43`  
		Last Modified: Wed, 26 Feb 2025 22:30:52 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3e69ad67d62bcf313d3f0d97ecf562c4bf5310aebc04819f5ba144174c995d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303839605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b8227a1a7b249a87483cddb9616bb5ae4ff122c1fd847884084a0e48340eb3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e79ef03a42dbe2876898f16a38c0286273d341eed88ff0c63ea5125c37c702e`  
		Last Modified: Wed, 26 Feb 2025 22:30:26 GMT  
		Size: 54.7 MB (54677213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff505137b20bd757addb3d29c71d8e254b1caea248ea9266e29c104824341c22`  
		Last Modified: Wed, 26 Feb 2025 22:30:24 GMT  
		Size: 1.5 MB (1488027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb529a1ffd698d3aa55bb2808f18abd18837ea54fc32158d29613fb3f1e0f6d7`  
		Last Modified: Wed, 26 Feb 2025 22:30:30 GMT  
		Size: 219.6 MB (219625908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7` - unknown; unknown

```console
$ docker pull dart@sha256:3991581d9bce6f45923638ff2548ff0c00e286acf0b87e0bddacdcb98fbeb64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ecd3f2c7f552541823962446115ae4723ea78ef00f4264043845dc4e12c370`

```dockerfile
```

-	Layers:
	-	`sha256:d2ab17a330033f2f7ee682e526d90b897f88c863e78575ef2b4efe6cce6eaf95`  
		Last Modified: Wed, 26 Feb 2025 22:30:24 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.7-sdk`

```console
$ docker pull dart@sha256:5d40556368d94af9a1b41447cf1e5635dec18dc3f52c66096e1561be6580a321
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
$ docker pull dart@sha256:8d3825a508394f0e9eaabb81e9eff8d52fcb23f55c842d08a648ee254d3879a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304930725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c9c9268d1361e6c26ef3dd09475bd80909fb46f07afe944beadd783107c101`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8f516bb78ef3ba2aaba44acb0935922bd5c8b107ee9eaba02150613734eaf9`  
		Last Modified: Wed, 26 Feb 2025 22:30:22 GMT  
		Size: 54.9 MB (54906797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aae2eb44aadb93c85b847cba6f77a5f4ccc2d100468e1f2fb2f63602840f5c`  
		Last Modified: Wed, 26 Feb 2025 22:30:20 GMT  
		Size: 1.8 MB (1796912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66854d8af3d8fdaf583800167c14ed49972798b625ccb8622ee8bea3d264a78`  
		Last Modified: Wed, 26 Feb 2025 22:30:26 GMT  
		Size: 220.0 MB (220007683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ddc154eddd84bf7937ae0eaab0fec5427fbfe56479440b9b513dc8bdf2168247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21231a7ac629ef3212c7d6adfc4cd2154f9375abd8688c9958f12e4fbdd0a40e`

```dockerfile
```

-	Layers:
	-	`sha256:45ce83ec221425122a41bacb4fdbb7139cf2c6ae9c0f9f585818c4c48ad44c2e`  
		Last Modified: Wed, 26 Feb 2025 22:30:20 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:a7567cde4ecc1ffea3e6418dab3d8f63dcbeadd0f77edb7dfe1a3f9fef375683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226295824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f45f579fbcd6f82488a20ef3cea4b92d9090a74b9583665ed2e0179c850c41`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a359f18382a9bcd45ac7a3c553332cd0869d70af84eecf35d256ad8e43693e`  
		Last Modified: Wed, 26 Feb 2025 22:30:54 GMT  
		Size: 49.6 MB (49561776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5175bf9db12ef7e7e9057eb5a889211ad5a0307eff0d459e22a21a7cffa3c33e`  
		Last Modified: Wed, 26 Feb 2025 22:30:53 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf06b0e14fb02b9d2b31bdf62ce720061b537522d8991850f51dcc8f47519874`  
		Last Modified: Wed, 26 Feb 2025 22:30:56 GMT  
		Size: 151.6 MB (151592607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e620675e509085d8c37353d4db6e3f3372d75d2c4f0596c0645c74aee686ecfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd7aedd8f4ef8ae28889e348df03e3d2961d4bcbe9b81f2edb92e6492d6d798`

```dockerfile
```

-	Layers:
	-	`sha256:6a91f3dbee63f59c739a877245c060505be61b4f23c1e73f4eb779f06d25ea43`  
		Last Modified: Wed, 26 Feb 2025 22:30:52 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3e69ad67d62bcf313d3f0d97ecf562c4bf5310aebc04819f5ba144174c995d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303839605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b8227a1a7b249a87483cddb9616bb5ae4ff122c1fd847884084a0e48340eb3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e79ef03a42dbe2876898f16a38c0286273d341eed88ff0c63ea5125c37c702e`  
		Last Modified: Wed, 26 Feb 2025 22:30:26 GMT  
		Size: 54.7 MB (54677213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff505137b20bd757addb3d29c71d8e254b1caea248ea9266e29c104824341c22`  
		Last Modified: Wed, 26 Feb 2025 22:30:24 GMT  
		Size: 1.5 MB (1488027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb529a1ffd698d3aa55bb2808f18abd18837ea54fc32158d29613fb3f1e0f6d7`  
		Last Modified: Wed, 26 Feb 2025 22:30:30 GMT  
		Size: 219.6 MB (219625908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:3991581d9bce6f45923638ff2548ff0c00e286acf0b87e0bddacdcb98fbeb64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ecd3f2c7f552541823962446115ae4723ea78ef00f4264043845dc4e12c370`

```dockerfile
```

-	Layers:
	-	`sha256:d2ab17a330033f2f7ee682e526d90b897f88c863e78575ef2b4efe6cce6eaf95`  
		Last Modified: Wed, 26 Feb 2025 22:30:24 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.7.1`

```console
$ docker pull dart@sha256:5d40556368d94af9a1b41447cf1e5635dec18dc3f52c66096e1561be6580a321
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.7.1` - linux; amd64

```console
$ docker pull dart@sha256:8d3825a508394f0e9eaabb81e9eff8d52fcb23f55c842d08a648ee254d3879a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304930725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c9c9268d1361e6c26ef3dd09475bd80909fb46f07afe944beadd783107c101`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8f516bb78ef3ba2aaba44acb0935922bd5c8b107ee9eaba02150613734eaf9`  
		Last Modified: Wed, 26 Feb 2025 22:30:22 GMT  
		Size: 54.9 MB (54906797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aae2eb44aadb93c85b847cba6f77a5f4ccc2d100468e1f2fb2f63602840f5c`  
		Last Modified: Wed, 26 Feb 2025 22:30:20 GMT  
		Size: 1.8 MB (1796912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66854d8af3d8fdaf583800167c14ed49972798b625ccb8622ee8bea3d264a78`  
		Last Modified: Wed, 26 Feb 2025 22:30:26 GMT  
		Size: 220.0 MB (220007683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.1` - unknown; unknown

```console
$ docker pull dart@sha256:ddc154eddd84bf7937ae0eaab0fec5427fbfe56479440b9b513dc8bdf2168247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21231a7ac629ef3212c7d6adfc4cd2154f9375abd8688c9958f12e4fbdd0a40e`

```dockerfile
```

-	Layers:
	-	`sha256:45ce83ec221425122a41bacb4fdbb7139cf2c6ae9c0f9f585818c4c48ad44c2e`  
		Last Modified: Wed, 26 Feb 2025 22:30:20 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7.1` - linux; arm variant v7

```console
$ docker pull dart@sha256:a7567cde4ecc1ffea3e6418dab3d8f63dcbeadd0f77edb7dfe1a3f9fef375683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226295824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f45f579fbcd6f82488a20ef3cea4b92d9090a74b9583665ed2e0179c850c41`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a359f18382a9bcd45ac7a3c553332cd0869d70af84eecf35d256ad8e43693e`  
		Last Modified: Wed, 26 Feb 2025 22:30:54 GMT  
		Size: 49.6 MB (49561776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5175bf9db12ef7e7e9057eb5a889211ad5a0307eff0d459e22a21a7cffa3c33e`  
		Last Modified: Wed, 26 Feb 2025 22:30:53 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf06b0e14fb02b9d2b31bdf62ce720061b537522d8991850f51dcc8f47519874`  
		Last Modified: Wed, 26 Feb 2025 22:30:56 GMT  
		Size: 151.6 MB (151592607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.1` - unknown; unknown

```console
$ docker pull dart@sha256:e620675e509085d8c37353d4db6e3f3372d75d2c4f0596c0645c74aee686ecfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd7aedd8f4ef8ae28889e348df03e3d2961d4bcbe9b81f2edb92e6492d6d798`

```dockerfile
```

-	Layers:
	-	`sha256:6a91f3dbee63f59c739a877245c060505be61b4f23c1e73f4eb779f06d25ea43`  
		Last Modified: Wed, 26 Feb 2025 22:30:52 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7.1` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3e69ad67d62bcf313d3f0d97ecf562c4bf5310aebc04819f5ba144174c995d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303839605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b8227a1a7b249a87483cddb9616bb5ae4ff122c1fd847884084a0e48340eb3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e79ef03a42dbe2876898f16a38c0286273d341eed88ff0c63ea5125c37c702e`  
		Last Modified: Wed, 26 Feb 2025 22:30:26 GMT  
		Size: 54.7 MB (54677213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff505137b20bd757addb3d29c71d8e254b1caea248ea9266e29c104824341c22`  
		Last Modified: Wed, 26 Feb 2025 22:30:24 GMT  
		Size: 1.5 MB (1488027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb529a1ffd698d3aa55bb2808f18abd18837ea54fc32158d29613fb3f1e0f6d7`  
		Last Modified: Wed, 26 Feb 2025 22:30:30 GMT  
		Size: 219.6 MB (219625908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.1` - unknown; unknown

```console
$ docker pull dart@sha256:3991581d9bce6f45923638ff2548ff0c00e286acf0b87e0bddacdcb98fbeb64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ecd3f2c7f552541823962446115ae4723ea78ef00f4264043845dc4e12c370`

```dockerfile
```

-	Layers:
	-	`sha256:d2ab17a330033f2f7ee682e526d90b897f88c863e78575ef2b4efe6cce6eaf95`  
		Last Modified: Wed, 26 Feb 2025 22:30:24 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.7.1-sdk`

```console
$ docker pull dart@sha256:5d40556368d94af9a1b41447cf1e5635dec18dc3f52c66096e1561be6580a321
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.7.1-sdk` - linux; amd64

```console
$ docker pull dart@sha256:8d3825a508394f0e9eaabb81e9eff8d52fcb23f55c842d08a648ee254d3879a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304930725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c9c9268d1361e6c26ef3dd09475bd80909fb46f07afe944beadd783107c101`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8f516bb78ef3ba2aaba44acb0935922bd5c8b107ee9eaba02150613734eaf9`  
		Last Modified: Wed, 26 Feb 2025 22:30:22 GMT  
		Size: 54.9 MB (54906797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aae2eb44aadb93c85b847cba6f77a5f4ccc2d100468e1f2fb2f63602840f5c`  
		Last Modified: Wed, 26 Feb 2025 22:30:20 GMT  
		Size: 1.8 MB (1796912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66854d8af3d8fdaf583800167c14ed49972798b625ccb8622ee8bea3d264a78`  
		Last Modified: Wed, 26 Feb 2025 22:30:26 GMT  
		Size: 220.0 MB (220007683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ddc154eddd84bf7937ae0eaab0fec5427fbfe56479440b9b513dc8bdf2168247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21231a7ac629ef3212c7d6adfc4cd2154f9375abd8688c9958f12e4fbdd0a40e`

```dockerfile
```

-	Layers:
	-	`sha256:45ce83ec221425122a41bacb4fdbb7139cf2c6ae9c0f9f585818c4c48ad44c2e`  
		Last Modified: Wed, 26 Feb 2025 22:30:20 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7.1-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:a7567cde4ecc1ffea3e6418dab3d8f63dcbeadd0f77edb7dfe1a3f9fef375683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226295824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f45f579fbcd6f82488a20ef3cea4b92d9090a74b9583665ed2e0179c850c41`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a359f18382a9bcd45ac7a3c553332cd0869d70af84eecf35d256ad8e43693e`  
		Last Modified: Wed, 26 Feb 2025 22:30:54 GMT  
		Size: 49.6 MB (49561776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5175bf9db12ef7e7e9057eb5a889211ad5a0307eff0d459e22a21a7cffa3c33e`  
		Last Modified: Wed, 26 Feb 2025 22:30:53 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf06b0e14fb02b9d2b31bdf62ce720061b537522d8991850f51dcc8f47519874`  
		Last Modified: Wed, 26 Feb 2025 22:30:56 GMT  
		Size: 151.6 MB (151592607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e620675e509085d8c37353d4db6e3f3372d75d2c4f0596c0645c74aee686ecfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd7aedd8f4ef8ae28889e348df03e3d2961d4bcbe9b81f2edb92e6492d6d798`

```dockerfile
```

-	Layers:
	-	`sha256:6a91f3dbee63f59c739a877245c060505be61b4f23c1e73f4eb779f06d25ea43`  
		Last Modified: Wed, 26 Feb 2025 22:30:52 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7.1-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3e69ad67d62bcf313d3f0d97ecf562c4bf5310aebc04819f5ba144174c995d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303839605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b8227a1a7b249a87483cddb9616bb5ae4ff122c1fd847884084a0e48340eb3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e79ef03a42dbe2876898f16a38c0286273d341eed88ff0c63ea5125c37c702e`  
		Last Modified: Wed, 26 Feb 2025 22:30:26 GMT  
		Size: 54.7 MB (54677213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff505137b20bd757addb3d29c71d8e254b1caea248ea9266e29c104824341c22`  
		Last Modified: Wed, 26 Feb 2025 22:30:24 GMT  
		Size: 1.5 MB (1488027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb529a1ffd698d3aa55bb2808f18abd18837ea54fc32158d29613fb3f1e0f6d7`  
		Last Modified: Wed, 26 Feb 2025 22:30:30 GMT  
		Size: 219.6 MB (219625908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:3991581d9bce6f45923638ff2548ff0c00e286acf0b87e0bddacdcb98fbeb64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ecd3f2c7f552541823962446115ae4723ea78ef00f4264043845dc4e12c370`

```dockerfile
```

-	Layers:
	-	`sha256:d2ab17a330033f2f7ee682e526d90b897f88c863e78575ef2b4efe6cce6eaf95`  
		Last Modified: Wed, 26 Feb 2025 22:30:24 GMT  
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
$ docker pull dart@sha256:5d40556368d94af9a1b41447cf1e5635dec18dc3f52c66096e1561be6580a321
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
$ docker pull dart@sha256:8d3825a508394f0e9eaabb81e9eff8d52fcb23f55c842d08a648ee254d3879a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304930725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c9c9268d1361e6c26ef3dd09475bd80909fb46f07afe944beadd783107c101`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8f516bb78ef3ba2aaba44acb0935922bd5c8b107ee9eaba02150613734eaf9`  
		Last Modified: Wed, 26 Feb 2025 22:30:22 GMT  
		Size: 54.9 MB (54906797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aae2eb44aadb93c85b847cba6f77a5f4ccc2d100468e1f2fb2f63602840f5c`  
		Last Modified: Wed, 26 Feb 2025 22:30:20 GMT  
		Size: 1.8 MB (1796912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66854d8af3d8fdaf583800167c14ed49972798b625ccb8622ee8bea3d264a78`  
		Last Modified: Wed, 26 Feb 2025 22:30:26 GMT  
		Size: 220.0 MB (220007683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:ddc154eddd84bf7937ae0eaab0fec5427fbfe56479440b9b513dc8bdf2168247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21231a7ac629ef3212c7d6adfc4cd2154f9375abd8688c9958f12e4fbdd0a40e`

```dockerfile
```

-	Layers:
	-	`sha256:45ce83ec221425122a41bacb4fdbb7139cf2c6ae9c0f9f585818c4c48ad44c2e`  
		Last Modified: Wed, 26 Feb 2025 22:30:20 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:a7567cde4ecc1ffea3e6418dab3d8f63dcbeadd0f77edb7dfe1a3f9fef375683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226295824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f45f579fbcd6f82488a20ef3cea4b92d9090a74b9583665ed2e0179c850c41`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a359f18382a9bcd45ac7a3c553332cd0869d70af84eecf35d256ad8e43693e`  
		Last Modified: Wed, 26 Feb 2025 22:30:54 GMT  
		Size: 49.6 MB (49561776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5175bf9db12ef7e7e9057eb5a889211ad5a0307eff0d459e22a21a7cffa3c33e`  
		Last Modified: Wed, 26 Feb 2025 22:30:53 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf06b0e14fb02b9d2b31bdf62ce720061b537522d8991850f51dcc8f47519874`  
		Last Modified: Wed, 26 Feb 2025 22:30:56 GMT  
		Size: 151.6 MB (151592607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:e620675e509085d8c37353d4db6e3f3372d75d2c4f0596c0645c74aee686ecfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd7aedd8f4ef8ae28889e348df03e3d2961d4bcbe9b81f2edb92e6492d6d798`

```dockerfile
```

-	Layers:
	-	`sha256:6a91f3dbee63f59c739a877245c060505be61b4f23c1e73f4eb779f06d25ea43`  
		Last Modified: Wed, 26 Feb 2025 22:30:52 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3e69ad67d62bcf313d3f0d97ecf562c4bf5310aebc04819f5ba144174c995d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303839605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b8227a1a7b249a87483cddb9616bb5ae4ff122c1fd847884084a0e48340eb3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e79ef03a42dbe2876898f16a38c0286273d341eed88ff0c63ea5125c37c702e`  
		Last Modified: Wed, 26 Feb 2025 22:30:26 GMT  
		Size: 54.7 MB (54677213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff505137b20bd757addb3d29c71d8e254b1caea248ea9266e29c104824341c22`  
		Last Modified: Wed, 26 Feb 2025 22:30:24 GMT  
		Size: 1.5 MB (1488027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb529a1ffd698d3aa55bb2808f18abd18837ea54fc32158d29613fb3f1e0f6d7`  
		Last Modified: Wed, 26 Feb 2025 22:30:30 GMT  
		Size: 219.6 MB (219625908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:3991581d9bce6f45923638ff2548ff0c00e286acf0b87e0bddacdcb98fbeb64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ecd3f2c7f552541823962446115ae4723ea78ef00f4264043845dc4e12c370`

```dockerfile
```

-	Layers:
	-	`sha256:d2ab17a330033f2f7ee682e526d90b897f88c863e78575ef2b4efe6cce6eaf95`  
		Last Modified: Wed, 26 Feb 2025 22:30:24 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:5d40556368d94af9a1b41447cf1e5635dec18dc3f52c66096e1561be6580a321
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
$ docker pull dart@sha256:8d3825a508394f0e9eaabb81e9eff8d52fcb23f55c842d08a648ee254d3879a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304930725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c9c9268d1361e6c26ef3dd09475bd80909fb46f07afe944beadd783107c101`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8f516bb78ef3ba2aaba44acb0935922bd5c8b107ee9eaba02150613734eaf9`  
		Last Modified: Wed, 26 Feb 2025 22:30:22 GMT  
		Size: 54.9 MB (54906797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aae2eb44aadb93c85b847cba6f77a5f4ccc2d100468e1f2fb2f63602840f5c`  
		Last Modified: Wed, 26 Feb 2025 22:30:20 GMT  
		Size: 1.8 MB (1796912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66854d8af3d8fdaf583800167c14ed49972798b625ccb8622ee8bea3d264a78`  
		Last Modified: Wed, 26 Feb 2025 22:30:26 GMT  
		Size: 220.0 MB (220007683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ddc154eddd84bf7937ae0eaab0fec5427fbfe56479440b9b513dc8bdf2168247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21231a7ac629ef3212c7d6adfc4cd2154f9375abd8688c9958f12e4fbdd0a40e`

```dockerfile
```

-	Layers:
	-	`sha256:45ce83ec221425122a41bacb4fdbb7139cf2c6ae9c0f9f585818c4c48ad44c2e`  
		Last Modified: Wed, 26 Feb 2025 22:30:20 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:a7567cde4ecc1ffea3e6418dab3d8f63dcbeadd0f77edb7dfe1a3f9fef375683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226295824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f45f579fbcd6f82488a20ef3cea4b92d9090a74b9583665ed2e0179c850c41`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a359f18382a9bcd45ac7a3c553332cd0869d70af84eecf35d256ad8e43693e`  
		Last Modified: Wed, 26 Feb 2025 22:30:54 GMT  
		Size: 49.6 MB (49561776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5175bf9db12ef7e7e9057eb5a889211ad5a0307eff0d459e22a21a7cffa3c33e`  
		Last Modified: Wed, 26 Feb 2025 22:30:53 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf06b0e14fb02b9d2b31bdf62ce720061b537522d8991850f51dcc8f47519874`  
		Last Modified: Wed, 26 Feb 2025 22:30:56 GMT  
		Size: 151.6 MB (151592607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e620675e509085d8c37353d4db6e3f3372d75d2c4f0596c0645c74aee686ecfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd7aedd8f4ef8ae28889e348df03e3d2961d4bcbe9b81f2edb92e6492d6d798`

```dockerfile
```

-	Layers:
	-	`sha256:6a91f3dbee63f59c739a877245c060505be61b4f23c1e73f4eb779f06d25ea43`  
		Last Modified: Wed, 26 Feb 2025 22:30:52 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3e69ad67d62bcf313d3f0d97ecf562c4bf5310aebc04819f5ba144174c995d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303839605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b8227a1a7b249a87483cddb9616bb5ae4ff122c1fd847884084a0e48340eb3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e79ef03a42dbe2876898f16a38c0286273d341eed88ff0c63ea5125c37c702e`  
		Last Modified: Wed, 26 Feb 2025 22:30:26 GMT  
		Size: 54.7 MB (54677213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff505137b20bd757addb3d29c71d8e254b1caea248ea9266e29c104824341c22`  
		Last Modified: Wed, 26 Feb 2025 22:30:24 GMT  
		Size: 1.5 MB (1488027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb529a1ffd698d3aa55bb2808f18abd18837ea54fc32158d29613fb3f1e0f6d7`  
		Last Modified: Wed, 26 Feb 2025 22:30:30 GMT  
		Size: 219.6 MB (219625908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:3991581d9bce6f45923638ff2548ff0c00e286acf0b87e0bddacdcb98fbeb64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ecd3f2c7f552541823962446115ae4723ea78ef00f4264043845dc4e12c370`

```dockerfile
```

-	Layers:
	-	`sha256:d2ab17a330033f2f7ee682e526d90b897f88c863e78575ef2b4efe6cce6eaf95`  
		Last Modified: Wed, 26 Feb 2025 22:30:24 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:5d40556368d94af9a1b41447cf1e5635dec18dc3f52c66096e1561be6580a321
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
$ docker pull dart@sha256:8d3825a508394f0e9eaabb81e9eff8d52fcb23f55c842d08a648ee254d3879a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304930725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c9c9268d1361e6c26ef3dd09475bd80909fb46f07afe944beadd783107c101`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8f516bb78ef3ba2aaba44acb0935922bd5c8b107ee9eaba02150613734eaf9`  
		Last Modified: Wed, 26 Feb 2025 22:30:22 GMT  
		Size: 54.9 MB (54906797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aae2eb44aadb93c85b847cba6f77a5f4ccc2d100468e1f2fb2f63602840f5c`  
		Last Modified: Wed, 26 Feb 2025 22:30:20 GMT  
		Size: 1.8 MB (1796912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66854d8af3d8fdaf583800167c14ed49972798b625ccb8622ee8bea3d264a78`  
		Last Modified: Wed, 26 Feb 2025 22:30:26 GMT  
		Size: 220.0 MB (220007683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:ddc154eddd84bf7937ae0eaab0fec5427fbfe56479440b9b513dc8bdf2168247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21231a7ac629ef3212c7d6adfc4cd2154f9375abd8688c9958f12e4fbdd0a40e`

```dockerfile
```

-	Layers:
	-	`sha256:45ce83ec221425122a41bacb4fdbb7139cf2c6ae9c0f9f585818c4c48ad44c2e`  
		Last Modified: Wed, 26 Feb 2025 22:30:20 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:a7567cde4ecc1ffea3e6418dab3d8f63dcbeadd0f77edb7dfe1a3f9fef375683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226295824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f45f579fbcd6f82488a20ef3cea4b92d9090a74b9583665ed2e0179c850c41`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a359f18382a9bcd45ac7a3c553332cd0869d70af84eecf35d256ad8e43693e`  
		Last Modified: Wed, 26 Feb 2025 22:30:54 GMT  
		Size: 49.6 MB (49561776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5175bf9db12ef7e7e9057eb5a889211ad5a0307eff0d459e22a21a7cffa3c33e`  
		Last Modified: Wed, 26 Feb 2025 22:30:53 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf06b0e14fb02b9d2b31bdf62ce720061b537522d8991850f51dcc8f47519874`  
		Last Modified: Wed, 26 Feb 2025 22:30:56 GMT  
		Size: 151.6 MB (151592607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:e620675e509085d8c37353d4db6e3f3372d75d2c4f0596c0645c74aee686ecfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd7aedd8f4ef8ae28889e348df03e3d2961d4bcbe9b81f2edb92e6492d6d798`

```dockerfile
```

-	Layers:
	-	`sha256:6a91f3dbee63f59c739a877245c060505be61b4f23c1e73f4eb779f06d25ea43`  
		Last Modified: Wed, 26 Feb 2025 22:30:52 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3e69ad67d62bcf313d3f0d97ecf562c4bf5310aebc04819f5ba144174c995d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303839605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b8227a1a7b249a87483cddb9616bb5ae4ff122c1fd847884084a0e48340eb3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e79ef03a42dbe2876898f16a38c0286273d341eed88ff0c63ea5125c37c702e`  
		Last Modified: Wed, 26 Feb 2025 22:30:26 GMT  
		Size: 54.7 MB (54677213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff505137b20bd757addb3d29c71d8e254b1caea248ea9266e29c104824341c22`  
		Last Modified: Wed, 26 Feb 2025 22:30:24 GMT  
		Size: 1.5 MB (1488027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb529a1ffd698d3aa55bb2808f18abd18837ea54fc32158d29613fb3f1e0f6d7`  
		Last Modified: Wed, 26 Feb 2025 22:30:30 GMT  
		Size: 219.6 MB (219625908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:3991581d9bce6f45923638ff2548ff0c00e286acf0b87e0bddacdcb98fbeb64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ecd3f2c7f552541823962446115ae4723ea78ef00f4264043845dc4e12c370`

```dockerfile
```

-	Layers:
	-	`sha256:d2ab17a330033f2f7ee682e526d90b897f88c863e78575ef2b4efe6cce6eaf95`  
		Last Modified: Wed, 26 Feb 2025 22:30:24 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:5d40556368d94af9a1b41447cf1e5635dec18dc3f52c66096e1561be6580a321
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
$ docker pull dart@sha256:8d3825a508394f0e9eaabb81e9eff8d52fcb23f55c842d08a648ee254d3879a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304930725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c9c9268d1361e6c26ef3dd09475bd80909fb46f07afe944beadd783107c101`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8f516bb78ef3ba2aaba44acb0935922bd5c8b107ee9eaba02150613734eaf9`  
		Last Modified: Wed, 26 Feb 2025 22:30:22 GMT  
		Size: 54.9 MB (54906797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aae2eb44aadb93c85b847cba6f77a5f4ccc2d100468e1f2fb2f63602840f5c`  
		Last Modified: Wed, 26 Feb 2025 22:30:20 GMT  
		Size: 1.8 MB (1796912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66854d8af3d8fdaf583800167c14ed49972798b625ccb8622ee8bea3d264a78`  
		Last Modified: Wed, 26 Feb 2025 22:30:26 GMT  
		Size: 220.0 MB (220007683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ddc154eddd84bf7937ae0eaab0fec5427fbfe56479440b9b513dc8bdf2168247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21231a7ac629ef3212c7d6adfc4cd2154f9375abd8688c9958f12e4fbdd0a40e`

```dockerfile
```

-	Layers:
	-	`sha256:45ce83ec221425122a41bacb4fdbb7139cf2c6ae9c0f9f585818c4c48ad44c2e`  
		Last Modified: Wed, 26 Feb 2025 22:30:20 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:a7567cde4ecc1ffea3e6418dab3d8f63dcbeadd0f77edb7dfe1a3f9fef375683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226295824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f45f579fbcd6f82488a20ef3cea4b92d9090a74b9583665ed2e0179c850c41`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a359f18382a9bcd45ac7a3c553332cd0869d70af84eecf35d256ad8e43693e`  
		Last Modified: Wed, 26 Feb 2025 22:30:54 GMT  
		Size: 49.6 MB (49561776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5175bf9db12ef7e7e9057eb5a889211ad5a0307eff0d459e22a21a7cffa3c33e`  
		Last Modified: Wed, 26 Feb 2025 22:30:53 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf06b0e14fb02b9d2b31bdf62ce720061b537522d8991850f51dcc8f47519874`  
		Last Modified: Wed, 26 Feb 2025 22:30:56 GMT  
		Size: 151.6 MB (151592607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e620675e509085d8c37353d4db6e3f3372d75d2c4f0596c0645c74aee686ecfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd7aedd8f4ef8ae28889e348df03e3d2961d4bcbe9b81f2edb92e6492d6d798`

```dockerfile
```

-	Layers:
	-	`sha256:6a91f3dbee63f59c739a877245c060505be61b4f23c1e73f4eb779f06d25ea43`  
		Last Modified: Wed, 26 Feb 2025 22:30:52 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3e69ad67d62bcf313d3f0d97ecf562c4bf5310aebc04819f5ba144174c995d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303839605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b8227a1a7b249a87483cddb9616bb5ae4ff122c1fd847884084a0e48340eb3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 26 Feb 2025 16:28:06 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Feb 2025 16:28:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 16:28:06 GMT
WORKDIR /root
# Wed, 26 Feb 2025 16:28:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2813959e7d9650334015b927cc533f5beadfbf7fa48248beec471f8942a0ee71;             SDK_ARCH="x64";;         armhf)             DART_SHA256=199ed39b5f5c90bd26f3d1560959a2a81786be752f779abc7e3f933fc149c890;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ea91ddbf7d0278b377e3c47175ce4f5da726e9a81d49b987f13eadcf969847fe;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e79ef03a42dbe2876898f16a38c0286273d341eed88ff0c63ea5125c37c702e`  
		Last Modified: Wed, 26 Feb 2025 22:30:26 GMT  
		Size: 54.7 MB (54677213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff505137b20bd757addb3d29c71d8e254b1caea248ea9266e29c104824341c22`  
		Last Modified: Wed, 26 Feb 2025 22:30:24 GMT  
		Size: 1.5 MB (1488027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb529a1ffd698d3aa55bb2808f18abd18837ea54fc32158d29613fb3f1e0f6d7`  
		Last Modified: Wed, 26 Feb 2025 22:30:30 GMT  
		Size: 219.6 MB (219625908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:3991581d9bce6f45923638ff2548ff0c00e286acf0b87e0bddacdcb98fbeb64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ecd3f2c7f552541823962446115ae4723ea78ef00f4264043845dc4e12c370`

```dockerfile
```

-	Layers:
	-	`sha256:d2ab17a330033f2f7ee682e526d90b897f88c863e78575ef2b4efe6cce6eaf95`  
		Last Modified: Wed, 26 Feb 2025 22:30:24 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json
