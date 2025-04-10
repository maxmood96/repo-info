## `dart:beta`

```console
$ docker pull dart@sha256:02d4f3b4582898526b157bf6d9c807add166e0d1ca550886c8d15f2768a12a2b
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
$ docker pull dart@sha256:01c09e4b756caed96ccff22a0745d70d1d28adb9c598bc70d79b211f62a8ad6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285796854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6578de743df85d3a00124c4a0e3c54e6891015df80f89277d2e0900cbbfb3e0a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 09 Apr 2025 08:41:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 08:41:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 09 Apr 2025 08:41:53 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 09 Apr 2025 08:41:53 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 08:41:53 GMT
WORKDIR /root
# Wed, 09 Apr 2025 08:41:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c2d0e8f50f0b2634cc2d1ba18c0341199f0d879d8fa489536887ddea77812cef;             SDK_ARCH="x64";;         armhf)             DART_SHA256=eb85834ef45179d946541470ba171a50f222435e6e96a149e3c2b403a6b7386d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=130cce8ba744a6d37fca8fe0f06f68cd3abc119f250386f41424d2ac333c2269;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-278.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc40524eaedc86f7fd0e29794dc081a1e56585ea9cb71f49b64edf6e1590ca3`  
		Last Modified: Thu, 10 Apr 2025 17:17:28 GMT  
		Size: 54.9 MB (54907853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa85806df89f23aa1d32cc6d2676de83c62f97e3a29a948ec59948fb53b2bc2`  
		Last Modified: Thu, 10 Apr 2025 17:17:26 GMT  
		Size: 1.8 MB (1785443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d26e570667a8c59389abc968d09bc63cc0b11e7965fd82eb1107fb904cc9ee`  
		Last Modified: Thu, 10 Apr 2025 17:17:31 GMT  
		Size: 200.9 MB (200876267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:8eccc2a4054d9966abb15c7aeec3a3f720bb7f774cfffb29781709a42bb1dbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c60e465518abcf87f13b1a93dff33819a8f9b70b7fd311026d3d1df0efb82e9`

```dockerfile
```

-	Layers:
	-	`sha256:ad6eb90b23aacc2ba18ec0ee005b8ecf34e78869b77a00560fa3b259c09cec1a`  
		Last Modified: Thu, 10 Apr 2025 17:17:26 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:d54d20a960129b8b0ab9ba34948d4beda1fb3bea60218b82dfa1a4c95971c242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214445440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094566d89b8ac0acc055d0dfd7bab2997f65faa91e3298aae69fbf69438dc031`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Wed, 09 Apr 2025 08:41:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 08:41:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 09 Apr 2025 08:41:53 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 09 Apr 2025 08:41:53 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 08:41:53 GMT
WORKDIR /root
# Wed, 09 Apr 2025 08:41:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c2d0e8f50f0b2634cc2d1ba18c0341199f0d879d8fa489536887ddea77812cef;             SDK_ARCH="x64";;         armhf)             DART_SHA256=eb85834ef45179d946541470ba171a50f222435e6e96a149e3c2b403a6b7386d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=130cce8ba744a6d37fca8fe0f06f68cd3abc119f250386f41424d2ac333c2269;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-278.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbbda8caf4f3826b7e84d6a15ec648cf08d7b19878ab083744a66923fd195a7`  
		Last Modified: Thu, 10 Apr 2025 17:18:44 GMT  
		Size: 49.6 MB (49562253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11b4aa75dccab0e8ec878ffc240ead54ec21bfc0b8a0abc8bfab91f269e4f09`  
		Last Modified: Thu, 10 Apr 2025 17:18:43 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d104cb8b501b0f51e50ca272b9096d1f39aacb74c485ec375c5f2454c8661f`  
		Last Modified: Thu, 10 Apr 2025 17:18:46 GMT  
		Size: 139.7 MB (139723344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:f9611379d1a45a0cdb805f38428f0e8497b601bea7d3b27e7fde63efb1702842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c323e689c1a2b078a7702be82d4f032d4fd103b9729d33416dff65ab725fb46d`

```dockerfile
```

-	Layers:
	-	`sha256:9739603364cd89d0e79258972f052e362173536fa371f079aa866e0b91accdce`  
		Last Modified: Thu, 10 Apr 2025 17:18:42 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:cc69bfaec771ac3db845094b14ce9f01c2ca5ed0ef5ceba41ce3ce98b2a85ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284359642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf1f22bcca1d21fb01bc4f60c976167daa96369de01a661cf55a8ecc28248cc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 09 Apr 2025 08:41:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 08:41:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 09 Apr 2025 08:41:53 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 09 Apr 2025 08:41:53 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 08:41:53 GMT
WORKDIR /root
# Wed, 09 Apr 2025 08:41:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c2d0e8f50f0b2634cc2d1ba18c0341199f0d879d8fa489536887ddea77812cef;             SDK_ARCH="x64";;         armhf)             DART_SHA256=eb85834ef45179d946541470ba171a50f222435e6e96a149e3c2b403a6b7386d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=130cce8ba744a6d37fca8fe0f06f68cd3abc119f250386f41424d2ac333c2269;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-278.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc28df026982faa9bfb950a3c7ccec77ce8d5558b7a8ff7e49274e422716069`  
		Last Modified: Thu, 10 Apr 2025 17:19:13 GMT  
		Size: 54.7 MB (54678943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13cd6c94b330f1b145fa15415d95454c63571887bd90946f35676d8566dc928`  
		Last Modified: Thu, 10 Apr 2025 17:19:11 GMT  
		Size: 1.5 MB (1488221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b10dc5360b7ab62ba6f28281a38618be9131a75cabf3ce7d6f8773e7bc7419`  
		Last Modified: Thu, 10 Apr 2025 17:19:16 GMT  
		Size: 200.1 MB (200126126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:eabcc56e69805f7d51026f1d9cae1994bc29ccfa8d656aa48db64e044d13e854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ccda347d2c19caeebf20ec776ca9e9657eb3af7930e02478dd2d66e8dc66df3`

```dockerfile
```

-	Layers:
	-	`sha256:248ba75d26f2d9221c7ae43f01963d040103fac5681ab55a2b836a157e0b1914`  
		Last Modified: Thu, 10 Apr 2025 17:19:11 GMT  
		Size: 18.0 KB (18044 bytes)  
		MIME: application/vnd.in-toto+json
