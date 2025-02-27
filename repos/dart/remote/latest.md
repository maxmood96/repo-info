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
