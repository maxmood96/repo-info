## `dart:beta`

```console
$ docker pull dart@sha256:76bd9906da39a98fe4c6f2313d63c5233dd94c10ebdc28c25dc151b836eada5e
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
$ docker pull dart@sha256:d32315fcb7b8b055dcdcef69551302b10f67b55d9d374eb0db99df70f3b0584d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297131903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b943e3be9cc6764b81065dd227b4ecf843d031b62b0cd1005495b81daf5c5c7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7208dc4e56e61267b6abd64b4b3bc238205cdc4fc7ca50f367f4c6d3124a22`  
		Last Modified: Thu, 27 Mar 2025 18:58:07 GMT  
		Size: 54.9 MB (54907949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b837a9baf8ae6347250659266900a3ed6f41e8a6bc7eaf55dbadbebd8a0dfc9`  
		Last Modified: Thu, 27 Mar 2025 18:58:06 GMT  
		Size: 1.8 MB (1785446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d759370cc20bed907a74e8788c5a8a7fccc63d7a6a261db2af3d0bdd7bebde9`  
		Last Modified: Thu, 27 Mar 2025 18:58:11 GMT  
		Size: 212.2 MB (212233611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:533b2c924d69d1e10eeb8cb4a038f868437d8f9e62e479dcc0ada9c60e2d2b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388a8128c909493614d2cb108b3f92c24a143abbabc082910ed815b73e3aba16`

```dockerfile
```

-	Layers:
	-	`sha256:7dabb2a068d1a9ccd39700253cfcc6f8ab1bb80a46b5aeecee63d1beb91bab46`  
		Last Modified: Thu, 27 Mar 2025 18:58:05 GMT  
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
