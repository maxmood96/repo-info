## `dart:beta-sdk`

```console
$ docker pull dart@sha256:1f12fbe83b6119b89adc809d522fb134653112113d8138c61f1adf3e00352fe1
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
$ docker pull dart@sha256:d14db02b1ddbad1227a94d523ac2692a2f9d63740d79930de41b28a058d6c3a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304940081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c592c1c68be72c2d6ecbd1b4122f51f0e5af18d4c92a45a9e973b32d92734e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 05 Feb 2025 12:06:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 05 Feb 2025 12:06:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Feb 2025 12:06:12 GMT
WORKDIR /root
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d6a462d124ac3b48c7a662b74a7502e734d00f51f815b2b311579c0078daccfd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=83562e543537e1a2410ecc9cbb048ef4cdaa94ab837787a3973aeed552f98fe8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d603f3a9020f64f59b68d8a746091c07afc38c8d8c23b0a75e21720a4da0bf4c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-323.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8d180a2a6fba525f6bd619575d9119dcf70231419419b82f262a31deb4170d`  
		Last Modified: Fri, 07 Feb 2025 01:28:38 GMT  
		Size: 54.9 MB (54906684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab1c62e6f1d8b54d7bfec96f9c4af7eaf5436894aecbd95abb271b5cde43d3d`  
		Last Modified: Fri, 07 Feb 2025 01:28:38 GMT  
		Size: 1.8 MB (1796897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6fb8af2a09fe17bd14d7d355fc84d14ba6749d73ee6730fb1b38f7442e42c0`  
		Last Modified: Fri, 07 Feb 2025 01:28:41 GMT  
		Size: 220.0 MB (220024165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:54fef2c13bd1d3f0f34cd044192249d55cec715a9d201c46b86c1edc46a020c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408c11a604dd86848dca581949a4eb197e37baf6270ee0608a02498ee64c14e6`

```dockerfile
```

-	Layers:
	-	`sha256:e8c72f97bbd24c33a08e9cd58023d27e293ed57372273c0ca60596bccaaa51a4`  
		Last Modified: Fri, 07 Feb 2025 01:28:38 GMT  
		Size: 17.9 KB (17910 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:314ee130f2d0d4784b0953032a591274f4380a953c332eda234212d04f09a241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226295420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4b7b4e08a9e7da1ac5b5745b7f5e08d25e7eb2b7793b4644d516d66c4c9948`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 05 Feb 2025 12:06:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 05 Feb 2025 12:06:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Feb 2025 12:06:12 GMT
WORKDIR /root
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d6a462d124ac3b48c7a662b74a7502e734d00f51f815b2b311579c0078daccfd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=83562e543537e1a2410ecc9cbb048ef4cdaa94ab837787a3973aeed552f98fe8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d603f3a9020f64f59b68d8a746091c07afc38c8d8c23b0a75e21720a4da0bf4c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-323.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8432744e96f8e3d90822a9a33b68fa65a289664ee5ac213442a4e52916168089`  
		Last Modified: Fri, 07 Feb 2025 03:20:03 GMT  
		Size: 49.6 MB (49561375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b710ff2c3b109be6fe938d2b7ab2cde4487ccf605b861e3cd5ee8c52d5cf0c25`  
		Last Modified: Fri, 07 Feb 2025 03:20:01 GMT  
		Size: 1.2 MB (1221678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc926946ea1a36a01be65a523b2a5078a83b9dd85bfe95c1f88c358a2bb8ab5b`  
		Last Modified: Fri, 07 Feb 2025 03:20:05 GMT  
		Size: 151.6 MB (151597799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ff0f6766ff68f48f7da8e34067e2850bf351341b70e26f2691866a6f28656beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc9e105b97c94793aaf63fc99b3a5cbfee3ebbb770b87fc95ffdc1862b3dddf`

```dockerfile
```

-	Layers:
	-	`sha256:152db1344dfce1d3003af153661bd40bd62ea9de0f9518292345478228ac9246`  
		Last Modified: Fri, 07 Feb 2025 03:20:01 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:9ed40e8759ed4d725aca2f1ef654914423071eece09fa7e71f87b174da338a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303810824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:030406127a8d09d377de8e299f33eaa37c8ba78bc535338837ea2a2c4b4a3a6b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 05 Feb 2025 12:06:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 05 Feb 2025 12:06:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Feb 2025 12:06:12 GMT
WORKDIR /root
# Wed, 05 Feb 2025 12:06:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d6a462d124ac3b48c7a662b74a7502e734d00f51f815b2b311579c0078daccfd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=83562e543537e1a2410ecc9cbb048ef4cdaa94ab837787a3973aeed552f98fe8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d603f3a9020f64f59b68d8a746091c07afc38c8d8c23b0a75e21720a4da0bf4c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-323.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58af1233d09bfad98bc960981cbc8881df170ee3f4214c372e90b53b6f7b450`  
		Last Modified: Fri, 07 Feb 2025 01:47:23 GMT  
		Size: 54.7 MB (54678608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc05226888eb43ebe8086d27d2f039bd73130b7ba6efb7a4bc0e04de959b9b4`  
		Last Modified: Fri, 07 Feb 2025 01:47:20 GMT  
		Size: 1.5 MB (1488034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0acb94c18e870be38c13c9d2dc0232b497146feb4f0d0b4c0094dc282f47fc`  
		Last Modified: Fri, 07 Feb 2025 01:47:26 GMT  
		Size: 219.6 MB (219603269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6e208e683e396fb324c932275493fda4f2d22f58c313f1913501ec1600f55dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13da8768fc95c82e9496554677235ad34fc68d9418b39adeef381b3f2dc0a78`

```dockerfile
```

-	Layers:
	-	`sha256:add612a755844b5eb0a49a979c39630599b813f742553c8867b070fa0600655a`  
		Last Modified: Fri, 07 Feb 2025 01:47:20 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json
