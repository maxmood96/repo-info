## `dart:stable`

```console
$ docker pull dart@sha256:6e280d1bbf1a3cb4da1ad2ff77307c6c8e5375d6fec155d1ea8734da6f03e5d6
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
$ docker pull dart@sha256:e94899f5c067fba78ddd8d96274673dd87b435197b55f42a28621b5189ef5629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305359280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2209e4637d78407a89f22dc1ce4e4a883026777444ded51f64580f835f323ee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa97965da0640a9420fa2aae78fc199db213ee7dfca98c556f6f1dae98027fc`  
		Last Modified: Mon, 17 Mar 2025 23:14:39 GMT  
		Size: 54.9 MB (54907949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb0504f8ee5be02fef3dcafd0db60750a1da245aa7aa14126d6cbb6d93f8e63`  
		Last Modified: Mon, 17 Mar 2025 23:14:38 GMT  
		Size: 1.8 MB (1785447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76a9a349fd3ed39e1dfeb48b7ee60cc93440137da2ee702b3f0c00509aa1695`  
		Last Modified: Mon, 17 Mar 2025 23:14:43 GMT  
		Size: 220.5 MB (220460987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:97fff261ff2e66aa3cfc5e331b31ffeb0557c1c01d7ae26434654ba79c17f574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2842fc05f535117d2af5c7c668bd87b41a18d404947b700de225f5d0e88e199`

```dockerfile
```

-	Layers:
	-	`sha256:30b63a228145cc36cba13eb2913e6dc57b9089df3520633118e86656bd0a5b8f`  
		Last Modified: Mon, 17 Mar 2025 23:14:37 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d9c927c152b2c3d87e3ac69afd6328f9831a2875f33dcc4cc4cd425c40f735b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226291105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2261335dcf37c21db7f023a0451fa4ecdbc75b1fb9d59b127dd7f060398ea7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c93b8fd21f16e455ea78d5bde6caa154201a29de8b46231a24c2add8c4617b`  
		Last Modified: Tue, 18 Mar 2025 06:31:14 GMT  
		Size: 49.6 MB (49561746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3c3c9f9d55928fead9f3a4da4831bf52da646fa70eeb43ecaec385a9c4b68d`  
		Last Modified: Tue, 18 Mar 2025 06:31:12 GMT  
		Size: 1.2 MB (1221938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce883cc8a1d5b91b14d7dc7d44b8107de304cef7c3c386149cc8d1e279ea9eb3`  
		Last Modified: Tue, 18 Mar 2025 06:31:16 GMT  
		Size: 151.6 MB (151592301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:e2eaee0b4542bba459542c17bf1b54bc120ed38a3ae9188f880c7d56b26231a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2823625c0f31d59bcaa795a19cff381dadba16d0b7dbb878c6c5a9a027e6543d`

```dockerfile
```

-	Layers:
	-	`sha256:7c42669dfe6ff893492a04fdddf54c8fa268ce6053f36c27b30a7c4fd129d247`  
		Last Modified: Tue, 18 Mar 2025 06:31:12 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:fa9072f808cb3c8ac1230498ac721ca055d5667a5e4e7c7f45dcd21a5bb8a5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303837214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b765cccbabb6cd73309fa9fd557e2e1ae8ac1eb7f7a0885e675c7c43b259a882`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c216fdd70f656c50c78dc6a0ffae6e5ced7a9a7ccedea3e402fa6b5ebe24788c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7376e09dbb66aa8af25423a67c36f0ccb771ee280f12ed8157f1e26095abe67e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3452ccad61e057eb7fa17e85ed1aa035d44c36e33dac07655717798f47e64ca8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0e44317139d437e3a0030b2a5681351b64688c925cabaf26c463eae756097d`  
		Last Modified: Tue, 18 Mar 2025 05:32:15 GMT  
		Size: 54.7 MB (54678888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e6ea165b50c90409bcc2021c84bb757614ecf3c10c11a0c866f97673091e36`  
		Last Modified: Tue, 18 Mar 2025 05:32:13 GMT  
		Size: 1.5 MB (1488212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12a2d23e63fd0ca0f9c767ac72fe75b2ff092e16511e166c978d9ad000246b9`  
		Last Modified: Tue, 18 Mar 2025 05:32:18 GMT  
		Size: 219.6 MB (219626045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:6f95762d375ba3eeae8aad857d442e2c220ee8fb9d163d2094effe5e2b5caaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d52c0a42000c08e48c92bca0cb052efe5fe4c425c94f38928e03a760d35c27a`

```dockerfile
```

-	Layers:
	-	`sha256:417cb0c8593799bfc188df240164693386c9ddfaa96d2ab8b1617c6bc857bed2`  
		Last Modified: Tue, 18 Mar 2025 05:32:13 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json
