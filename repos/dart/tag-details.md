<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.8`](#dart38)
-	[`dart:3.8-sdk`](#dart38-sdk)
-	[`dart:3.8.1`](#dart381)
-	[`dart:3.8.1-sdk`](#dart381-sdk)
-	[`dart:3.9.0-196.1.beta`](#dart390-1961beta)
-	[`dart:3.9.0-196.1.beta-sdk`](#dart390-1961beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:5675e2e8e963024328dedc075af5eec0824f1f0c9728ef0f0c673ea098efac79
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
$ docker pull dart@sha256:2fdf4ee8914e661e714243fecef04625354febc8f527e7194baa78f23566bd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285802648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383978bad3d34de5e093cc36e7e574bb41eef7f6b53d898789b0fe4dd75c6a57`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758698419310856f0fdd07e1d59d6227640490bfa69978d7e37c9bb5d19697c2`  
		Last Modified: Tue, 01 Jul 2025 02:26:27 GMT  
		Size: 54.9 MB (54920852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e01113bdd1f9cd91dddfd1b2af92a0a37607fca21f83c0098ece68db8f3cc2`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 1.8 MB (1787570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c98b4987321144ec38891b065b34cd8d806402f81ac6c8fc6c35a5900078b2`  
		Last Modified: Tue, 01 Jul 2025 05:53:49 GMT  
		Size: 200.9 MB (200864051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:647c843711afc163c783c0712d20d68c72b12035ce8e4838dfe0437ca0755b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b869c16bd3ad98c33fe9a5620313d04fa5315048e4d6a02ebdc34dc188300d6`

```dockerfile
```

-	Layers:
	-	`sha256:22839f67ae69cd8b5450dc94985dc09c61f099e68ffd7346f0e8165aefb16df9`  
		Last Modified: Tue, 01 Jul 2025 05:53:19 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:30961b78a9455044cdeebd8e41454f7826ae0890d1ecc0e442c2261047955a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214495629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7616f113838f66551152abbaa7e78bb1b6290da0165f1e95a33db5ee79db4ecd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a384e57dc162d271c967993ad51c536042f8fa44021c63d2f1e1451d01d3c`  
		Last Modified: Tue, 01 Jul 2025 09:03:37 GMT  
		Size: 49.6 MB (49556735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee7d20d2503756c5a0cea91dd771363af7976637e4c7611f6483e765d74e31`  
		Last Modified: Tue, 01 Jul 2025 09:03:29 GMT  
		Size: 1.2 MB (1224878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e97106d5b222a68acbdae51583cfc0a75ba53e01f57bdb345f142a5f9ff64a0`  
		Last Modified: Tue, 01 Jul 2025 09:12:28 GMT  
		Size: 139.8 MB (139775240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:b69fd6a56114da5a99b236eb4b08821c7967d3ccd4d6bcc8522d997ea6540db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedf7f483396412ba0b566c8f047fd67ece80adfa19c540b1fc89e776393bc63`

```dockerfile
```

-	Layers:
	-	`sha256:d1f48b8093c2678f6877cdd055da43ced65e56e5d5f64328d9b3b5774e406c40`  
		Last Modified: Tue, 01 Jul 2025 11:53:22 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:6c4ba78803afed3f4f89c2e1cb5f7eeefc11bdf7621520a532cee3f394436549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284486186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ec929ca46b8fa33558ef4129121da8c2572970244cc227a5328014eee31ce3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69c2715daafc240c33dedb398493c36f5697dc53cc8c9ef8c66db70503b768c`  
		Last Modified: Tue, 01 Jul 2025 06:59:17 GMT  
		Size: 54.7 MB (54695649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f06f85123f3f957451b79d3bc63ba1b3045a3fcb3d921481b36f1ae11892087`  
		Last Modified: Tue, 01 Jul 2025 06:59:00 GMT  
		Size: 1.5 MB (1491204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f53f4a2356e25368725c1421c7511b559baf5914ac33118f66a54e4505a229`  
		Last Modified: Tue, 01 Jul 2025 08:27:52 GMT  
		Size: 200.2 MB (200221623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:a98ad7aa9bce661ceb25b3b6342582bbdfda5ee7de83b719c329d36a1b1e8fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804bc826bf83e4d5dc041066aa7c1725dec624ca6cfc78a1f6cd23b92535c2c7`

```dockerfile
```

-	Layers:
	-	`sha256:736f01326d3c430d8d8fc479826197a5abcac1b1c6e61191cee9620f5d06b45a`  
		Last Modified: Tue, 01 Jul 2025 08:53:22 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:5675e2e8e963024328dedc075af5eec0824f1f0c9728ef0f0c673ea098efac79
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
$ docker pull dart@sha256:2fdf4ee8914e661e714243fecef04625354febc8f527e7194baa78f23566bd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285802648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383978bad3d34de5e093cc36e7e574bb41eef7f6b53d898789b0fe4dd75c6a57`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758698419310856f0fdd07e1d59d6227640490bfa69978d7e37c9bb5d19697c2`  
		Last Modified: Tue, 01 Jul 2025 02:26:27 GMT  
		Size: 54.9 MB (54920852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e01113bdd1f9cd91dddfd1b2af92a0a37607fca21f83c0098ece68db8f3cc2`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 1.8 MB (1787570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c98b4987321144ec38891b065b34cd8d806402f81ac6c8fc6c35a5900078b2`  
		Last Modified: Tue, 01 Jul 2025 05:53:49 GMT  
		Size: 200.9 MB (200864051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:647c843711afc163c783c0712d20d68c72b12035ce8e4838dfe0437ca0755b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b869c16bd3ad98c33fe9a5620313d04fa5315048e4d6a02ebdc34dc188300d6`

```dockerfile
```

-	Layers:
	-	`sha256:22839f67ae69cd8b5450dc94985dc09c61f099e68ffd7346f0e8165aefb16df9`  
		Last Modified: Tue, 01 Jul 2025 05:53:19 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:30961b78a9455044cdeebd8e41454f7826ae0890d1ecc0e442c2261047955a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214495629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7616f113838f66551152abbaa7e78bb1b6290da0165f1e95a33db5ee79db4ecd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a384e57dc162d271c967993ad51c536042f8fa44021c63d2f1e1451d01d3c`  
		Last Modified: Tue, 01 Jul 2025 09:03:37 GMT  
		Size: 49.6 MB (49556735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee7d20d2503756c5a0cea91dd771363af7976637e4c7611f6483e765d74e31`  
		Last Modified: Tue, 01 Jul 2025 09:03:29 GMT  
		Size: 1.2 MB (1224878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e97106d5b222a68acbdae51583cfc0a75ba53e01f57bdb345f142a5f9ff64a0`  
		Last Modified: Tue, 01 Jul 2025 09:12:28 GMT  
		Size: 139.8 MB (139775240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b69fd6a56114da5a99b236eb4b08821c7967d3ccd4d6bcc8522d997ea6540db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedf7f483396412ba0b566c8f047fd67ece80adfa19c540b1fc89e776393bc63`

```dockerfile
```

-	Layers:
	-	`sha256:d1f48b8093c2678f6877cdd055da43ced65e56e5d5f64328d9b3b5774e406c40`  
		Last Modified: Tue, 01 Jul 2025 11:53:22 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:6c4ba78803afed3f4f89c2e1cb5f7eeefc11bdf7621520a532cee3f394436549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284486186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ec929ca46b8fa33558ef4129121da8c2572970244cc227a5328014eee31ce3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69c2715daafc240c33dedb398493c36f5697dc53cc8c9ef8c66db70503b768c`  
		Last Modified: Tue, 01 Jul 2025 06:59:17 GMT  
		Size: 54.7 MB (54695649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f06f85123f3f957451b79d3bc63ba1b3045a3fcb3d921481b36f1ae11892087`  
		Last Modified: Tue, 01 Jul 2025 06:59:00 GMT  
		Size: 1.5 MB (1491204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f53f4a2356e25368725c1421c7511b559baf5914ac33118f66a54e4505a229`  
		Last Modified: Tue, 01 Jul 2025 08:27:52 GMT  
		Size: 200.2 MB (200221623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a98ad7aa9bce661ceb25b3b6342582bbdfda5ee7de83b719c329d36a1b1e8fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804bc826bf83e4d5dc041066aa7c1725dec624ca6cfc78a1f6cd23b92535c2c7`

```dockerfile
```

-	Layers:
	-	`sha256:736f01326d3c430d8d8fc479826197a5abcac1b1c6e61191cee9620f5d06b45a`  
		Last Modified: Tue, 01 Jul 2025 08:53:22 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8`

```console
$ docker pull dart@sha256:5675e2e8e963024328dedc075af5eec0824f1f0c9728ef0f0c673ea098efac79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.8` - linux; amd64

```console
$ docker pull dart@sha256:2fdf4ee8914e661e714243fecef04625354febc8f527e7194baa78f23566bd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285802648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383978bad3d34de5e093cc36e7e574bb41eef7f6b53d898789b0fe4dd75c6a57`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758698419310856f0fdd07e1d59d6227640490bfa69978d7e37c9bb5d19697c2`  
		Last Modified: Tue, 01 Jul 2025 02:26:27 GMT  
		Size: 54.9 MB (54920852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e01113bdd1f9cd91dddfd1b2af92a0a37607fca21f83c0098ece68db8f3cc2`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 1.8 MB (1787570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c98b4987321144ec38891b065b34cd8d806402f81ac6c8fc6c35a5900078b2`  
		Last Modified: Tue, 01 Jul 2025 05:53:49 GMT  
		Size: 200.9 MB (200864051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8` - unknown; unknown

```console
$ docker pull dart@sha256:647c843711afc163c783c0712d20d68c72b12035ce8e4838dfe0437ca0755b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b869c16bd3ad98c33fe9a5620313d04fa5315048e4d6a02ebdc34dc188300d6`

```dockerfile
```

-	Layers:
	-	`sha256:22839f67ae69cd8b5450dc94985dc09c61f099e68ffd7346f0e8165aefb16df9`  
		Last Modified: Tue, 01 Jul 2025 05:53:19 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8` - linux; arm variant v7

```console
$ docker pull dart@sha256:30961b78a9455044cdeebd8e41454f7826ae0890d1ecc0e442c2261047955a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214495629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7616f113838f66551152abbaa7e78bb1b6290da0165f1e95a33db5ee79db4ecd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a384e57dc162d271c967993ad51c536042f8fa44021c63d2f1e1451d01d3c`  
		Last Modified: Tue, 01 Jul 2025 09:03:37 GMT  
		Size: 49.6 MB (49556735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee7d20d2503756c5a0cea91dd771363af7976637e4c7611f6483e765d74e31`  
		Last Modified: Tue, 01 Jul 2025 09:03:29 GMT  
		Size: 1.2 MB (1224878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e97106d5b222a68acbdae51583cfc0a75ba53e01f57bdb345f142a5f9ff64a0`  
		Last Modified: Tue, 01 Jul 2025 09:12:28 GMT  
		Size: 139.8 MB (139775240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8` - unknown; unknown

```console
$ docker pull dart@sha256:b69fd6a56114da5a99b236eb4b08821c7967d3ccd4d6bcc8522d997ea6540db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedf7f483396412ba0b566c8f047fd67ece80adfa19c540b1fc89e776393bc63`

```dockerfile
```

-	Layers:
	-	`sha256:d1f48b8093c2678f6877cdd055da43ced65e56e5d5f64328d9b3b5774e406c40`  
		Last Modified: Tue, 01 Jul 2025 11:53:22 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:6c4ba78803afed3f4f89c2e1cb5f7eeefc11bdf7621520a532cee3f394436549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284486186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ec929ca46b8fa33558ef4129121da8c2572970244cc227a5328014eee31ce3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69c2715daafc240c33dedb398493c36f5697dc53cc8c9ef8c66db70503b768c`  
		Last Modified: Tue, 01 Jul 2025 06:59:17 GMT  
		Size: 54.7 MB (54695649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f06f85123f3f957451b79d3bc63ba1b3045a3fcb3d921481b36f1ae11892087`  
		Last Modified: Tue, 01 Jul 2025 06:59:00 GMT  
		Size: 1.5 MB (1491204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f53f4a2356e25368725c1421c7511b559baf5914ac33118f66a54e4505a229`  
		Last Modified: Tue, 01 Jul 2025 08:27:52 GMT  
		Size: 200.2 MB (200221623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8` - unknown; unknown

```console
$ docker pull dart@sha256:a98ad7aa9bce661ceb25b3b6342582bbdfda5ee7de83b719c329d36a1b1e8fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804bc826bf83e4d5dc041066aa7c1725dec624ca6cfc78a1f6cd23b92535c2c7`

```dockerfile
```

-	Layers:
	-	`sha256:736f01326d3c430d8d8fc479826197a5abcac1b1c6e61191cee9620f5d06b45a`  
		Last Modified: Tue, 01 Jul 2025 08:53:22 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8-sdk`

```console
$ docker pull dart@sha256:5675e2e8e963024328dedc075af5eec0824f1f0c9728ef0f0c673ea098efac79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.8-sdk` - linux; amd64

```console
$ docker pull dart@sha256:2fdf4ee8914e661e714243fecef04625354febc8f527e7194baa78f23566bd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285802648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383978bad3d34de5e093cc36e7e574bb41eef7f6b53d898789b0fe4dd75c6a57`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758698419310856f0fdd07e1d59d6227640490bfa69978d7e37c9bb5d19697c2`  
		Last Modified: Tue, 01 Jul 2025 02:26:27 GMT  
		Size: 54.9 MB (54920852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e01113bdd1f9cd91dddfd1b2af92a0a37607fca21f83c0098ece68db8f3cc2`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 1.8 MB (1787570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c98b4987321144ec38891b065b34cd8d806402f81ac6c8fc6c35a5900078b2`  
		Last Modified: Tue, 01 Jul 2025 05:53:49 GMT  
		Size: 200.9 MB (200864051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:647c843711afc163c783c0712d20d68c72b12035ce8e4838dfe0437ca0755b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b869c16bd3ad98c33fe9a5620313d04fa5315048e4d6a02ebdc34dc188300d6`

```dockerfile
```

-	Layers:
	-	`sha256:22839f67ae69cd8b5450dc94985dc09c61f099e68ffd7346f0e8165aefb16df9`  
		Last Modified: Tue, 01 Jul 2025 05:53:19 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:30961b78a9455044cdeebd8e41454f7826ae0890d1ecc0e442c2261047955a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214495629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7616f113838f66551152abbaa7e78bb1b6290da0165f1e95a33db5ee79db4ecd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a384e57dc162d271c967993ad51c536042f8fa44021c63d2f1e1451d01d3c`  
		Last Modified: Tue, 01 Jul 2025 09:03:37 GMT  
		Size: 49.6 MB (49556735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee7d20d2503756c5a0cea91dd771363af7976637e4c7611f6483e765d74e31`  
		Last Modified: Tue, 01 Jul 2025 09:03:29 GMT  
		Size: 1.2 MB (1224878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e97106d5b222a68acbdae51583cfc0a75ba53e01f57bdb345f142a5f9ff64a0`  
		Last Modified: Tue, 01 Jul 2025 09:12:28 GMT  
		Size: 139.8 MB (139775240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b69fd6a56114da5a99b236eb4b08821c7967d3ccd4d6bcc8522d997ea6540db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedf7f483396412ba0b566c8f047fd67ece80adfa19c540b1fc89e776393bc63`

```dockerfile
```

-	Layers:
	-	`sha256:d1f48b8093c2678f6877cdd055da43ced65e56e5d5f64328d9b3b5774e406c40`  
		Last Modified: Tue, 01 Jul 2025 11:53:22 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:6c4ba78803afed3f4f89c2e1cb5f7eeefc11bdf7621520a532cee3f394436549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284486186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ec929ca46b8fa33558ef4129121da8c2572970244cc227a5328014eee31ce3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69c2715daafc240c33dedb398493c36f5697dc53cc8c9ef8c66db70503b768c`  
		Last Modified: Tue, 01 Jul 2025 06:59:17 GMT  
		Size: 54.7 MB (54695649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f06f85123f3f957451b79d3bc63ba1b3045a3fcb3d921481b36f1ae11892087`  
		Last Modified: Tue, 01 Jul 2025 06:59:00 GMT  
		Size: 1.5 MB (1491204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f53f4a2356e25368725c1421c7511b559baf5914ac33118f66a54e4505a229`  
		Last Modified: Tue, 01 Jul 2025 08:27:52 GMT  
		Size: 200.2 MB (200221623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a98ad7aa9bce661ceb25b3b6342582bbdfda5ee7de83b719c329d36a1b1e8fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804bc826bf83e4d5dc041066aa7c1725dec624ca6cfc78a1f6cd23b92535c2c7`

```dockerfile
```

-	Layers:
	-	`sha256:736f01326d3c430d8d8fc479826197a5abcac1b1c6e61191cee9620f5d06b45a`  
		Last Modified: Tue, 01 Jul 2025 08:53:22 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8.1`

```console
$ docker pull dart@sha256:5675e2e8e963024328dedc075af5eec0824f1f0c9728ef0f0c673ea098efac79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.8.1` - linux; amd64

```console
$ docker pull dart@sha256:2fdf4ee8914e661e714243fecef04625354febc8f527e7194baa78f23566bd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285802648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383978bad3d34de5e093cc36e7e574bb41eef7f6b53d898789b0fe4dd75c6a57`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758698419310856f0fdd07e1d59d6227640490bfa69978d7e37c9bb5d19697c2`  
		Last Modified: Tue, 01 Jul 2025 02:26:27 GMT  
		Size: 54.9 MB (54920852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e01113bdd1f9cd91dddfd1b2af92a0a37607fca21f83c0098ece68db8f3cc2`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 1.8 MB (1787570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c98b4987321144ec38891b065b34cd8d806402f81ac6c8fc6c35a5900078b2`  
		Last Modified: Tue, 01 Jul 2025 05:53:49 GMT  
		Size: 200.9 MB (200864051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.1` - unknown; unknown

```console
$ docker pull dart@sha256:647c843711afc163c783c0712d20d68c72b12035ce8e4838dfe0437ca0755b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b869c16bd3ad98c33fe9a5620313d04fa5315048e4d6a02ebdc34dc188300d6`

```dockerfile
```

-	Layers:
	-	`sha256:22839f67ae69cd8b5450dc94985dc09c61f099e68ffd7346f0e8165aefb16df9`  
		Last Modified: Tue, 01 Jul 2025 05:53:19 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.1` - linux; arm variant v7

```console
$ docker pull dart@sha256:30961b78a9455044cdeebd8e41454f7826ae0890d1ecc0e442c2261047955a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214495629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7616f113838f66551152abbaa7e78bb1b6290da0165f1e95a33db5ee79db4ecd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a384e57dc162d271c967993ad51c536042f8fa44021c63d2f1e1451d01d3c`  
		Last Modified: Tue, 01 Jul 2025 09:03:37 GMT  
		Size: 49.6 MB (49556735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee7d20d2503756c5a0cea91dd771363af7976637e4c7611f6483e765d74e31`  
		Last Modified: Tue, 01 Jul 2025 09:03:29 GMT  
		Size: 1.2 MB (1224878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e97106d5b222a68acbdae51583cfc0a75ba53e01f57bdb345f142a5f9ff64a0`  
		Last Modified: Tue, 01 Jul 2025 09:12:28 GMT  
		Size: 139.8 MB (139775240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.1` - unknown; unknown

```console
$ docker pull dart@sha256:b69fd6a56114da5a99b236eb4b08821c7967d3ccd4d6bcc8522d997ea6540db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedf7f483396412ba0b566c8f047fd67ece80adfa19c540b1fc89e776393bc63`

```dockerfile
```

-	Layers:
	-	`sha256:d1f48b8093c2678f6877cdd055da43ced65e56e5d5f64328d9b3b5774e406c40`  
		Last Modified: Tue, 01 Jul 2025 11:53:22 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.1` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:6c4ba78803afed3f4f89c2e1cb5f7eeefc11bdf7621520a532cee3f394436549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284486186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ec929ca46b8fa33558ef4129121da8c2572970244cc227a5328014eee31ce3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69c2715daafc240c33dedb398493c36f5697dc53cc8c9ef8c66db70503b768c`  
		Last Modified: Tue, 01 Jul 2025 06:59:17 GMT  
		Size: 54.7 MB (54695649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f06f85123f3f957451b79d3bc63ba1b3045a3fcb3d921481b36f1ae11892087`  
		Last Modified: Tue, 01 Jul 2025 06:59:00 GMT  
		Size: 1.5 MB (1491204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f53f4a2356e25368725c1421c7511b559baf5914ac33118f66a54e4505a229`  
		Last Modified: Tue, 01 Jul 2025 08:27:52 GMT  
		Size: 200.2 MB (200221623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.1` - unknown; unknown

```console
$ docker pull dart@sha256:a98ad7aa9bce661ceb25b3b6342582bbdfda5ee7de83b719c329d36a1b1e8fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804bc826bf83e4d5dc041066aa7c1725dec624ca6cfc78a1f6cd23b92535c2c7`

```dockerfile
```

-	Layers:
	-	`sha256:736f01326d3c430d8d8fc479826197a5abcac1b1c6e61191cee9620f5d06b45a`  
		Last Modified: Tue, 01 Jul 2025 08:53:22 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8.1-sdk`

```console
$ docker pull dart@sha256:5675e2e8e963024328dedc075af5eec0824f1f0c9728ef0f0c673ea098efac79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.8.1-sdk` - linux; amd64

```console
$ docker pull dart@sha256:2fdf4ee8914e661e714243fecef04625354febc8f527e7194baa78f23566bd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285802648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383978bad3d34de5e093cc36e7e574bb41eef7f6b53d898789b0fe4dd75c6a57`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758698419310856f0fdd07e1d59d6227640490bfa69978d7e37c9bb5d19697c2`  
		Last Modified: Tue, 01 Jul 2025 02:26:27 GMT  
		Size: 54.9 MB (54920852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e01113bdd1f9cd91dddfd1b2af92a0a37607fca21f83c0098ece68db8f3cc2`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 1.8 MB (1787570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c98b4987321144ec38891b065b34cd8d806402f81ac6c8fc6c35a5900078b2`  
		Last Modified: Tue, 01 Jul 2025 05:53:49 GMT  
		Size: 200.9 MB (200864051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:647c843711afc163c783c0712d20d68c72b12035ce8e4838dfe0437ca0755b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b869c16bd3ad98c33fe9a5620313d04fa5315048e4d6a02ebdc34dc188300d6`

```dockerfile
```

-	Layers:
	-	`sha256:22839f67ae69cd8b5450dc94985dc09c61f099e68ffd7346f0e8165aefb16df9`  
		Last Modified: Tue, 01 Jul 2025 05:53:19 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.1-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:30961b78a9455044cdeebd8e41454f7826ae0890d1ecc0e442c2261047955a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214495629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7616f113838f66551152abbaa7e78bb1b6290da0165f1e95a33db5ee79db4ecd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a384e57dc162d271c967993ad51c536042f8fa44021c63d2f1e1451d01d3c`  
		Last Modified: Tue, 01 Jul 2025 09:03:37 GMT  
		Size: 49.6 MB (49556735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee7d20d2503756c5a0cea91dd771363af7976637e4c7611f6483e765d74e31`  
		Last Modified: Tue, 01 Jul 2025 09:03:29 GMT  
		Size: 1.2 MB (1224878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e97106d5b222a68acbdae51583cfc0a75ba53e01f57bdb345f142a5f9ff64a0`  
		Last Modified: Tue, 01 Jul 2025 09:12:28 GMT  
		Size: 139.8 MB (139775240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b69fd6a56114da5a99b236eb4b08821c7967d3ccd4d6bcc8522d997ea6540db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedf7f483396412ba0b566c8f047fd67ece80adfa19c540b1fc89e776393bc63`

```dockerfile
```

-	Layers:
	-	`sha256:d1f48b8093c2678f6877cdd055da43ced65e56e5d5f64328d9b3b5774e406c40`  
		Last Modified: Tue, 01 Jul 2025 11:53:22 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.1-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:6c4ba78803afed3f4f89c2e1cb5f7eeefc11bdf7621520a532cee3f394436549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284486186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ec929ca46b8fa33558ef4129121da8c2572970244cc227a5328014eee31ce3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69c2715daafc240c33dedb398493c36f5697dc53cc8c9ef8c66db70503b768c`  
		Last Modified: Tue, 01 Jul 2025 06:59:17 GMT  
		Size: 54.7 MB (54695649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f06f85123f3f957451b79d3bc63ba1b3045a3fcb3d921481b36f1ae11892087`  
		Last Modified: Tue, 01 Jul 2025 06:59:00 GMT  
		Size: 1.5 MB (1491204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f53f4a2356e25368725c1421c7511b559baf5914ac33118f66a54e4505a229`  
		Last Modified: Tue, 01 Jul 2025 08:27:52 GMT  
		Size: 200.2 MB (200221623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a98ad7aa9bce661ceb25b3b6342582bbdfda5ee7de83b719c329d36a1b1e8fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804bc826bf83e4d5dc041066aa7c1725dec624ca6cfc78a1f6cd23b92535c2c7`

```dockerfile
```

-	Layers:
	-	`sha256:736f01326d3c430d8d8fc479826197a5abcac1b1c6e61191cee9620f5d06b45a`  
		Last Modified: Tue, 01 Jul 2025 08:53:22 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9.0-196.1.beta`

```console
$ docker pull dart@sha256:c1512af8a3f577f39a9d5a0aff31124d32743c0fef62263a14775be532603411
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.9.0-196.1.beta` - linux; amd64

```console
$ docker pull dart@sha256:f2a89089f57a37f48066a9b4995d9a7b062cf48389a690771494443613f753d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.5 MB (304500559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89489437634ec4836e24928c7c2dc4586ec8e33fb1787a540d1ba1fb46d9f3bd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d97e026a18428748fc3b4fd7762a6e6b03c44954ba5245d7ebef448832ad3efc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51522ceae050f3d6aeedd6a3702992daa34d8aca6e316ef8c33e46e3a3656ea6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e60b9ffd7b5fe2bbc8ee35c492521ba6bc07c94bac64ae7199ca77df737d61a3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-196.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77aeca5296302670eb7a9eddd452086cd78e1e027fa7c8b477601fb3aac94b0d`  
		Last Modified: Tue, 01 Jul 2025 05:53:50 GMT  
		Size: 54.9 MB (54920788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439a01a223bb95bb41f7871f57dfe99e3438f3d58bc2857ca83aa05db389417`  
		Last Modified: Tue, 01 Jul 2025 02:34:18 GMT  
		Size: 1.8 MB (1787572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e54c00c731fd9053ed181536b3c859c82f6670d303a4e0ea7d244e92a71a19`  
		Last Modified: Tue, 01 Jul 2025 05:53:53 GMT  
		Size: 219.6 MB (219562024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-196.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:1fe3c6393537588d6cb6f06164cf9191a82876213047a43909d5312e22168718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dd935b1a414706f022fbc84547494bcc3ca538bc9d85cb973ff5fa1d20f47d`

```dockerfile
```

-	Layers:
	-	`sha256:32292d02c63c40e898af6480dfc23165af57d06dd0fe849fdbdcec8137cfc23c`  
		Last Modified: Tue, 01 Jul 2025 05:53:33 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.0-196.1.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:fe7495f659d4c94c18d321b65b9d2a3fef98dcc9a7c5a025db9f32833b0630eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228492679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28143825cac80aa66ed480f41f18048a4a2baa79942abf06a7297b80f15ea36d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d97e026a18428748fc3b4fd7762a6e6b03c44954ba5245d7ebef448832ad3efc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51522ceae050f3d6aeedd6a3702992daa34d8aca6e316ef8c33e46e3a3656ea6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e60b9ffd7b5fe2bbc8ee35c492521ba6bc07c94bac64ae7199ca77df737d61a3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-196.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a384e57dc162d271c967993ad51c536042f8fa44021c63d2f1e1451d01d3c`  
		Last Modified: Tue, 01 Jul 2025 09:03:37 GMT  
		Size: 49.6 MB (49556735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee7d20d2503756c5a0cea91dd771363af7976637e4c7611f6483e765d74e31`  
		Last Modified: Tue, 01 Jul 2025 09:03:29 GMT  
		Size: 1.2 MB (1224878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54cf14626c44cbbf6c8cdad8192439621a2898fad741460adf06bb3b3154985`  
		Last Modified: Tue, 01 Jul 2025 11:53:49 GMT  
		Size: 153.8 MB (153772290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-196.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:631aa673f3fc79ff77071df4cb0f8ca24253c67f32f147fb34eb48a32852dcc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0ec9c76a84329a726eed350d9264a92e24e6807de9b7397802ce1499609404`

```dockerfile
```

-	Layers:
	-	`sha256:888caaf0a5e7f8286320bfdde4894939f26a1b8b9b95cf249af4134cf115b5b4`  
		Last Modified: Tue, 01 Jul 2025 11:53:33 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.0-196.1.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:ee558f38fb054213bea071b28b15587867f7c50332ac76acc0361520c063b05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303254678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5d668a2a75863e658bc893eb254a9e45b1f3d7b53e012ed3ed2d62f7f5a4f7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d97e026a18428748fc3b4fd7762a6e6b03c44954ba5245d7ebef448832ad3efc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51522ceae050f3d6aeedd6a3702992daa34d8aca6e316ef8c33e46e3a3656ea6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e60b9ffd7b5fe2bbc8ee35c492521ba6bc07c94bac64ae7199ca77df737d61a3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-196.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69c2715daafc240c33dedb398493c36f5697dc53cc8c9ef8c66db70503b768c`  
		Last Modified: Tue, 01 Jul 2025 06:59:17 GMT  
		Size: 54.7 MB (54695649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f06f85123f3f957451b79d3bc63ba1b3045a3fcb3d921481b36f1ae11892087`  
		Last Modified: Tue, 01 Jul 2025 06:59:00 GMT  
		Size: 1.5 MB (1491204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b2a435ae5ec37df02cc46e6a5df94377941628c6f79aa7c96884f475bf80f0`  
		Last Modified: Tue, 01 Jul 2025 08:53:50 GMT  
		Size: 219.0 MB (218990115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-196.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:7845f73d13c802709c88fc56934cdd37fa43f5203fbda3a8e3488134b606eeba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b75f32deab3b7f88c6d60f529d47efc054e66c17bd43597a26af8662c5ee218`

```dockerfile
```

-	Layers:
	-	`sha256:4af825a41ce9bbe06b2d2254cd376a6f99c3dd0f33306395805c13375437d2a9`  
		Last Modified: Tue, 01 Jul 2025 08:53:32 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9.0-196.1.beta-sdk`

```console
$ docker pull dart@sha256:c1512af8a3f577f39a9d5a0aff31124d32743c0fef62263a14775be532603411
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.9.0-196.1.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:f2a89089f57a37f48066a9b4995d9a7b062cf48389a690771494443613f753d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.5 MB (304500559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89489437634ec4836e24928c7c2dc4586ec8e33fb1787a540d1ba1fb46d9f3bd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d97e026a18428748fc3b4fd7762a6e6b03c44954ba5245d7ebef448832ad3efc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51522ceae050f3d6aeedd6a3702992daa34d8aca6e316ef8c33e46e3a3656ea6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e60b9ffd7b5fe2bbc8ee35c492521ba6bc07c94bac64ae7199ca77df737d61a3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-196.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77aeca5296302670eb7a9eddd452086cd78e1e027fa7c8b477601fb3aac94b0d`  
		Last Modified: Tue, 01 Jul 2025 05:53:50 GMT  
		Size: 54.9 MB (54920788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439a01a223bb95bb41f7871f57dfe99e3438f3d58bc2857ca83aa05db389417`  
		Last Modified: Tue, 01 Jul 2025 02:34:18 GMT  
		Size: 1.8 MB (1787572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e54c00c731fd9053ed181536b3c859c82f6670d303a4e0ea7d244e92a71a19`  
		Last Modified: Tue, 01 Jul 2025 05:53:53 GMT  
		Size: 219.6 MB (219562024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-196.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1fe3c6393537588d6cb6f06164cf9191a82876213047a43909d5312e22168718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dd935b1a414706f022fbc84547494bcc3ca538bc9d85cb973ff5fa1d20f47d`

```dockerfile
```

-	Layers:
	-	`sha256:32292d02c63c40e898af6480dfc23165af57d06dd0fe849fdbdcec8137cfc23c`  
		Last Modified: Tue, 01 Jul 2025 05:53:33 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.0-196.1.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:fe7495f659d4c94c18d321b65b9d2a3fef98dcc9a7c5a025db9f32833b0630eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228492679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28143825cac80aa66ed480f41f18048a4a2baa79942abf06a7297b80f15ea36d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d97e026a18428748fc3b4fd7762a6e6b03c44954ba5245d7ebef448832ad3efc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51522ceae050f3d6aeedd6a3702992daa34d8aca6e316ef8c33e46e3a3656ea6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e60b9ffd7b5fe2bbc8ee35c492521ba6bc07c94bac64ae7199ca77df737d61a3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-196.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a384e57dc162d271c967993ad51c536042f8fa44021c63d2f1e1451d01d3c`  
		Last Modified: Tue, 01 Jul 2025 09:03:37 GMT  
		Size: 49.6 MB (49556735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee7d20d2503756c5a0cea91dd771363af7976637e4c7611f6483e765d74e31`  
		Last Modified: Tue, 01 Jul 2025 09:03:29 GMT  
		Size: 1.2 MB (1224878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54cf14626c44cbbf6c8cdad8192439621a2898fad741460adf06bb3b3154985`  
		Last Modified: Tue, 01 Jul 2025 11:53:49 GMT  
		Size: 153.8 MB (153772290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-196.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:631aa673f3fc79ff77071df4cb0f8ca24253c67f32f147fb34eb48a32852dcc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0ec9c76a84329a726eed350d9264a92e24e6807de9b7397802ce1499609404`

```dockerfile
```

-	Layers:
	-	`sha256:888caaf0a5e7f8286320bfdde4894939f26a1b8b9b95cf249af4134cf115b5b4`  
		Last Modified: Tue, 01 Jul 2025 11:53:33 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.0-196.1.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:ee558f38fb054213bea071b28b15587867f7c50332ac76acc0361520c063b05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303254678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5d668a2a75863e658bc893eb254a9e45b1f3d7b53e012ed3ed2d62f7f5a4f7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d97e026a18428748fc3b4fd7762a6e6b03c44954ba5245d7ebef448832ad3efc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51522ceae050f3d6aeedd6a3702992daa34d8aca6e316ef8c33e46e3a3656ea6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e60b9ffd7b5fe2bbc8ee35c492521ba6bc07c94bac64ae7199ca77df737d61a3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-196.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69c2715daafc240c33dedb398493c36f5697dc53cc8c9ef8c66db70503b768c`  
		Last Modified: Tue, 01 Jul 2025 06:59:17 GMT  
		Size: 54.7 MB (54695649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f06f85123f3f957451b79d3bc63ba1b3045a3fcb3d921481b36f1ae11892087`  
		Last Modified: Tue, 01 Jul 2025 06:59:00 GMT  
		Size: 1.5 MB (1491204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b2a435ae5ec37df02cc46e6a5df94377941628c6f79aa7c96884f475bf80f0`  
		Last Modified: Tue, 01 Jul 2025 08:53:50 GMT  
		Size: 219.0 MB (218990115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-196.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7845f73d13c802709c88fc56934cdd37fa43f5203fbda3a8e3488134b606eeba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b75f32deab3b7f88c6d60f529d47efc054e66c17bd43597a26af8662c5ee218`

```dockerfile
```

-	Layers:
	-	`sha256:4af825a41ce9bbe06b2d2254cd376a6f99c3dd0f33306395805c13375437d2a9`  
		Last Modified: Tue, 01 Jul 2025 08:53:32 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:c1512af8a3f577f39a9d5a0aff31124d32743c0fef62263a14775be532603411
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
$ docker pull dart@sha256:f2a89089f57a37f48066a9b4995d9a7b062cf48389a690771494443613f753d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.5 MB (304500559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89489437634ec4836e24928c7c2dc4586ec8e33fb1787a540d1ba1fb46d9f3bd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d97e026a18428748fc3b4fd7762a6e6b03c44954ba5245d7ebef448832ad3efc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51522ceae050f3d6aeedd6a3702992daa34d8aca6e316ef8c33e46e3a3656ea6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e60b9ffd7b5fe2bbc8ee35c492521ba6bc07c94bac64ae7199ca77df737d61a3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-196.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77aeca5296302670eb7a9eddd452086cd78e1e027fa7c8b477601fb3aac94b0d`  
		Last Modified: Tue, 01 Jul 2025 05:53:50 GMT  
		Size: 54.9 MB (54920788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439a01a223bb95bb41f7871f57dfe99e3438f3d58bc2857ca83aa05db389417`  
		Last Modified: Tue, 01 Jul 2025 02:34:18 GMT  
		Size: 1.8 MB (1787572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e54c00c731fd9053ed181536b3c859c82f6670d303a4e0ea7d244e92a71a19`  
		Last Modified: Tue, 01 Jul 2025 05:53:53 GMT  
		Size: 219.6 MB (219562024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:1fe3c6393537588d6cb6f06164cf9191a82876213047a43909d5312e22168718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dd935b1a414706f022fbc84547494bcc3ca538bc9d85cb973ff5fa1d20f47d`

```dockerfile
```

-	Layers:
	-	`sha256:32292d02c63c40e898af6480dfc23165af57d06dd0fe849fdbdcec8137cfc23c`  
		Last Modified: Tue, 01 Jul 2025 05:53:33 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:fe7495f659d4c94c18d321b65b9d2a3fef98dcc9a7c5a025db9f32833b0630eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228492679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28143825cac80aa66ed480f41f18048a4a2baa79942abf06a7297b80f15ea36d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d97e026a18428748fc3b4fd7762a6e6b03c44954ba5245d7ebef448832ad3efc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51522ceae050f3d6aeedd6a3702992daa34d8aca6e316ef8c33e46e3a3656ea6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e60b9ffd7b5fe2bbc8ee35c492521ba6bc07c94bac64ae7199ca77df737d61a3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-196.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a384e57dc162d271c967993ad51c536042f8fa44021c63d2f1e1451d01d3c`  
		Last Modified: Tue, 01 Jul 2025 09:03:37 GMT  
		Size: 49.6 MB (49556735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee7d20d2503756c5a0cea91dd771363af7976637e4c7611f6483e765d74e31`  
		Last Modified: Tue, 01 Jul 2025 09:03:29 GMT  
		Size: 1.2 MB (1224878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54cf14626c44cbbf6c8cdad8192439621a2898fad741460adf06bb3b3154985`  
		Last Modified: Tue, 01 Jul 2025 11:53:49 GMT  
		Size: 153.8 MB (153772290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:631aa673f3fc79ff77071df4cb0f8ca24253c67f32f147fb34eb48a32852dcc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0ec9c76a84329a726eed350d9264a92e24e6807de9b7397802ce1499609404`

```dockerfile
```

-	Layers:
	-	`sha256:888caaf0a5e7f8286320bfdde4894939f26a1b8b9b95cf249af4134cf115b5b4`  
		Last Modified: Tue, 01 Jul 2025 11:53:33 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:ee558f38fb054213bea071b28b15587867f7c50332ac76acc0361520c063b05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303254678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5d668a2a75863e658bc893eb254a9e45b1f3d7b53e012ed3ed2d62f7f5a4f7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d97e026a18428748fc3b4fd7762a6e6b03c44954ba5245d7ebef448832ad3efc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51522ceae050f3d6aeedd6a3702992daa34d8aca6e316ef8c33e46e3a3656ea6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e60b9ffd7b5fe2bbc8ee35c492521ba6bc07c94bac64ae7199ca77df737d61a3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-196.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69c2715daafc240c33dedb398493c36f5697dc53cc8c9ef8c66db70503b768c`  
		Last Modified: Tue, 01 Jul 2025 06:59:17 GMT  
		Size: 54.7 MB (54695649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f06f85123f3f957451b79d3bc63ba1b3045a3fcb3d921481b36f1ae11892087`  
		Last Modified: Tue, 01 Jul 2025 06:59:00 GMT  
		Size: 1.5 MB (1491204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b2a435ae5ec37df02cc46e6a5df94377941628c6f79aa7c96884f475bf80f0`  
		Last Modified: Tue, 01 Jul 2025 08:53:50 GMT  
		Size: 219.0 MB (218990115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:7845f73d13c802709c88fc56934cdd37fa43f5203fbda3a8e3488134b606eeba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b75f32deab3b7f88c6d60f529d47efc054e66c17bd43597a26af8662c5ee218`

```dockerfile
```

-	Layers:
	-	`sha256:4af825a41ce9bbe06b2d2254cd376a6f99c3dd0f33306395805c13375437d2a9`  
		Last Modified: Tue, 01 Jul 2025 08:53:32 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:c1512af8a3f577f39a9d5a0aff31124d32743c0fef62263a14775be532603411
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
$ docker pull dart@sha256:f2a89089f57a37f48066a9b4995d9a7b062cf48389a690771494443613f753d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.5 MB (304500559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89489437634ec4836e24928c7c2dc4586ec8e33fb1787a540d1ba1fb46d9f3bd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d97e026a18428748fc3b4fd7762a6e6b03c44954ba5245d7ebef448832ad3efc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51522ceae050f3d6aeedd6a3702992daa34d8aca6e316ef8c33e46e3a3656ea6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e60b9ffd7b5fe2bbc8ee35c492521ba6bc07c94bac64ae7199ca77df737d61a3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-196.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77aeca5296302670eb7a9eddd452086cd78e1e027fa7c8b477601fb3aac94b0d`  
		Last Modified: Tue, 01 Jul 2025 05:53:50 GMT  
		Size: 54.9 MB (54920788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439a01a223bb95bb41f7871f57dfe99e3438f3d58bc2857ca83aa05db389417`  
		Last Modified: Tue, 01 Jul 2025 02:34:18 GMT  
		Size: 1.8 MB (1787572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e54c00c731fd9053ed181536b3c859c82f6670d303a4e0ea7d244e92a71a19`  
		Last Modified: Tue, 01 Jul 2025 05:53:53 GMT  
		Size: 219.6 MB (219562024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1fe3c6393537588d6cb6f06164cf9191a82876213047a43909d5312e22168718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dd935b1a414706f022fbc84547494bcc3ca538bc9d85cb973ff5fa1d20f47d`

```dockerfile
```

-	Layers:
	-	`sha256:32292d02c63c40e898af6480dfc23165af57d06dd0fe849fdbdcec8137cfc23c`  
		Last Modified: Tue, 01 Jul 2025 05:53:33 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:fe7495f659d4c94c18d321b65b9d2a3fef98dcc9a7c5a025db9f32833b0630eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228492679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28143825cac80aa66ed480f41f18048a4a2baa79942abf06a7297b80f15ea36d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d97e026a18428748fc3b4fd7762a6e6b03c44954ba5245d7ebef448832ad3efc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51522ceae050f3d6aeedd6a3702992daa34d8aca6e316ef8c33e46e3a3656ea6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e60b9ffd7b5fe2bbc8ee35c492521ba6bc07c94bac64ae7199ca77df737d61a3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-196.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a384e57dc162d271c967993ad51c536042f8fa44021c63d2f1e1451d01d3c`  
		Last Modified: Tue, 01 Jul 2025 09:03:37 GMT  
		Size: 49.6 MB (49556735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee7d20d2503756c5a0cea91dd771363af7976637e4c7611f6483e765d74e31`  
		Last Modified: Tue, 01 Jul 2025 09:03:29 GMT  
		Size: 1.2 MB (1224878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54cf14626c44cbbf6c8cdad8192439621a2898fad741460adf06bb3b3154985`  
		Last Modified: Tue, 01 Jul 2025 11:53:49 GMT  
		Size: 153.8 MB (153772290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:631aa673f3fc79ff77071df4cb0f8ca24253c67f32f147fb34eb48a32852dcc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0ec9c76a84329a726eed350d9264a92e24e6807de9b7397802ce1499609404`

```dockerfile
```

-	Layers:
	-	`sha256:888caaf0a5e7f8286320bfdde4894939f26a1b8b9b95cf249af4134cf115b5b4`  
		Last Modified: Tue, 01 Jul 2025 11:53:33 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:ee558f38fb054213bea071b28b15587867f7c50332ac76acc0361520c063b05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303254678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5d668a2a75863e658bc893eb254a9e45b1f3d7b53e012ed3ed2d62f7f5a4f7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d97e026a18428748fc3b4fd7762a6e6b03c44954ba5245d7ebef448832ad3efc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51522ceae050f3d6aeedd6a3702992daa34d8aca6e316ef8c33e46e3a3656ea6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e60b9ffd7b5fe2bbc8ee35c492521ba6bc07c94bac64ae7199ca77df737d61a3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-196.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69c2715daafc240c33dedb398493c36f5697dc53cc8c9ef8c66db70503b768c`  
		Last Modified: Tue, 01 Jul 2025 06:59:17 GMT  
		Size: 54.7 MB (54695649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f06f85123f3f957451b79d3bc63ba1b3045a3fcb3d921481b36f1ae11892087`  
		Last Modified: Tue, 01 Jul 2025 06:59:00 GMT  
		Size: 1.5 MB (1491204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b2a435ae5ec37df02cc46e6a5df94377941628c6f79aa7c96884f475bf80f0`  
		Last Modified: Tue, 01 Jul 2025 08:53:50 GMT  
		Size: 219.0 MB (218990115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7845f73d13c802709c88fc56934cdd37fa43f5203fbda3a8e3488134b606eeba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b75f32deab3b7f88c6d60f529d47efc054e66c17bd43597a26af8662c5ee218`

```dockerfile
```

-	Layers:
	-	`sha256:4af825a41ce9bbe06b2d2254cd376a6f99c3dd0f33306395805c13375437d2a9`  
		Last Modified: Tue, 01 Jul 2025 08:53:32 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:5675e2e8e963024328dedc075af5eec0824f1f0c9728ef0f0c673ea098efac79
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
$ docker pull dart@sha256:2fdf4ee8914e661e714243fecef04625354febc8f527e7194baa78f23566bd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285802648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383978bad3d34de5e093cc36e7e574bb41eef7f6b53d898789b0fe4dd75c6a57`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758698419310856f0fdd07e1d59d6227640490bfa69978d7e37c9bb5d19697c2`  
		Last Modified: Tue, 01 Jul 2025 02:26:27 GMT  
		Size: 54.9 MB (54920852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e01113bdd1f9cd91dddfd1b2af92a0a37607fca21f83c0098ece68db8f3cc2`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 1.8 MB (1787570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c98b4987321144ec38891b065b34cd8d806402f81ac6c8fc6c35a5900078b2`  
		Last Modified: Tue, 01 Jul 2025 05:53:49 GMT  
		Size: 200.9 MB (200864051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:647c843711afc163c783c0712d20d68c72b12035ce8e4838dfe0437ca0755b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b869c16bd3ad98c33fe9a5620313d04fa5315048e4d6a02ebdc34dc188300d6`

```dockerfile
```

-	Layers:
	-	`sha256:22839f67ae69cd8b5450dc94985dc09c61f099e68ffd7346f0e8165aefb16df9`  
		Last Modified: Tue, 01 Jul 2025 05:53:19 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:30961b78a9455044cdeebd8e41454f7826ae0890d1ecc0e442c2261047955a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214495629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7616f113838f66551152abbaa7e78bb1b6290da0165f1e95a33db5ee79db4ecd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a384e57dc162d271c967993ad51c536042f8fa44021c63d2f1e1451d01d3c`  
		Last Modified: Tue, 01 Jul 2025 09:03:37 GMT  
		Size: 49.6 MB (49556735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee7d20d2503756c5a0cea91dd771363af7976637e4c7611f6483e765d74e31`  
		Last Modified: Tue, 01 Jul 2025 09:03:29 GMT  
		Size: 1.2 MB (1224878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e97106d5b222a68acbdae51583cfc0a75ba53e01f57bdb345f142a5f9ff64a0`  
		Last Modified: Tue, 01 Jul 2025 09:12:28 GMT  
		Size: 139.8 MB (139775240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:b69fd6a56114da5a99b236eb4b08821c7967d3ccd4d6bcc8522d997ea6540db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedf7f483396412ba0b566c8f047fd67ece80adfa19c540b1fc89e776393bc63`

```dockerfile
```

-	Layers:
	-	`sha256:d1f48b8093c2678f6877cdd055da43ced65e56e5d5f64328d9b3b5774e406c40`  
		Last Modified: Tue, 01 Jul 2025 11:53:22 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:6c4ba78803afed3f4f89c2e1cb5f7eeefc11bdf7621520a532cee3f394436549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284486186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ec929ca46b8fa33558ef4129121da8c2572970244cc227a5328014eee31ce3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69c2715daafc240c33dedb398493c36f5697dc53cc8c9ef8c66db70503b768c`  
		Last Modified: Tue, 01 Jul 2025 06:59:17 GMT  
		Size: 54.7 MB (54695649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f06f85123f3f957451b79d3bc63ba1b3045a3fcb3d921481b36f1ae11892087`  
		Last Modified: Tue, 01 Jul 2025 06:59:00 GMT  
		Size: 1.5 MB (1491204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f53f4a2356e25368725c1421c7511b559baf5914ac33118f66a54e4505a229`  
		Last Modified: Tue, 01 Jul 2025 08:27:52 GMT  
		Size: 200.2 MB (200221623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:a98ad7aa9bce661ceb25b3b6342582bbdfda5ee7de83b719c329d36a1b1e8fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804bc826bf83e4d5dc041066aa7c1725dec624ca6cfc78a1f6cd23b92535c2c7`

```dockerfile
```

-	Layers:
	-	`sha256:736f01326d3c430d8d8fc479826197a5abcac1b1c6e61191cee9620f5d06b45a`  
		Last Modified: Tue, 01 Jul 2025 08:53:22 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:5675e2e8e963024328dedc075af5eec0824f1f0c9728ef0f0c673ea098efac79
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
$ docker pull dart@sha256:2fdf4ee8914e661e714243fecef04625354febc8f527e7194baa78f23566bd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285802648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383978bad3d34de5e093cc36e7e574bb41eef7f6b53d898789b0fe4dd75c6a57`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758698419310856f0fdd07e1d59d6227640490bfa69978d7e37c9bb5d19697c2`  
		Last Modified: Tue, 01 Jul 2025 02:26:27 GMT  
		Size: 54.9 MB (54920852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e01113bdd1f9cd91dddfd1b2af92a0a37607fca21f83c0098ece68db8f3cc2`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 1.8 MB (1787570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c98b4987321144ec38891b065b34cd8d806402f81ac6c8fc6c35a5900078b2`  
		Last Modified: Tue, 01 Jul 2025 05:53:49 GMT  
		Size: 200.9 MB (200864051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:647c843711afc163c783c0712d20d68c72b12035ce8e4838dfe0437ca0755b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b869c16bd3ad98c33fe9a5620313d04fa5315048e4d6a02ebdc34dc188300d6`

```dockerfile
```

-	Layers:
	-	`sha256:22839f67ae69cd8b5450dc94985dc09c61f099e68ffd7346f0e8165aefb16df9`  
		Last Modified: Tue, 01 Jul 2025 05:53:19 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:30961b78a9455044cdeebd8e41454f7826ae0890d1ecc0e442c2261047955a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214495629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7616f113838f66551152abbaa7e78bb1b6290da0165f1e95a33db5ee79db4ecd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a384e57dc162d271c967993ad51c536042f8fa44021c63d2f1e1451d01d3c`  
		Last Modified: Tue, 01 Jul 2025 09:03:37 GMT  
		Size: 49.6 MB (49556735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee7d20d2503756c5a0cea91dd771363af7976637e4c7611f6483e765d74e31`  
		Last Modified: Tue, 01 Jul 2025 09:03:29 GMT  
		Size: 1.2 MB (1224878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e97106d5b222a68acbdae51583cfc0a75ba53e01f57bdb345f142a5f9ff64a0`  
		Last Modified: Tue, 01 Jul 2025 09:12:28 GMT  
		Size: 139.8 MB (139775240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b69fd6a56114da5a99b236eb4b08821c7967d3ccd4d6bcc8522d997ea6540db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedf7f483396412ba0b566c8f047fd67ece80adfa19c540b1fc89e776393bc63`

```dockerfile
```

-	Layers:
	-	`sha256:d1f48b8093c2678f6877cdd055da43ced65e56e5d5f64328d9b3b5774e406c40`  
		Last Modified: Tue, 01 Jul 2025 11:53:22 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:6c4ba78803afed3f4f89c2e1cb5f7eeefc11bdf7621520a532cee3f394436549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284486186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ec929ca46b8fa33558ef4129121da8c2572970244cc227a5328014eee31ce3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69c2715daafc240c33dedb398493c36f5697dc53cc8c9ef8c66db70503b768c`  
		Last Modified: Tue, 01 Jul 2025 06:59:17 GMT  
		Size: 54.7 MB (54695649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f06f85123f3f957451b79d3bc63ba1b3045a3fcb3d921481b36f1ae11892087`  
		Last Modified: Tue, 01 Jul 2025 06:59:00 GMT  
		Size: 1.5 MB (1491204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f53f4a2356e25368725c1421c7511b559baf5914ac33118f66a54e4505a229`  
		Last Modified: Tue, 01 Jul 2025 08:27:52 GMT  
		Size: 200.2 MB (200221623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a98ad7aa9bce661ceb25b3b6342582bbdfda5ee7de83b719c329d36a1b1e8fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804bc826bf83e4d5dc041066aa7c1725dec624ca6cfc78a1f6cd23b92535c2c7`

```dockerfile
```

-	Layers:
	-	`sha256:736f01326d3c430d8d8fc479826197a5abcac1b1c6e61191cee9620f5d06b45a`  
		Last Modified: Tue, 01 Jul 2025 08:53:22 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:5675e2e8e963024328dedc075af5eec0824f1f0c9728ef0f0c673ea098efac79
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
$ docker pull dart@sha256:2fdf4ee8914e661e714243fecef04625354febc8f527e7194baa78f23566bd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285802648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383978bad3d34de5e093cc36e7e574bb41eef7f6b53d898789b0fe4dd75c6a57`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758698419310856f0fdd07e1d59d6227640490bfa69978d7e37c9bb5d19697c2`  
		Last Modified: Tue, 01 Jul 2025 02:26:27 GMT  
		Size: 54.9 MB (54920852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e01113bdd1f9cd91dddfd1b2af92a0a37607fca21f83c0098ece68db8f3cc2`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 1.8 MB (1787570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c98b4987321144ec38891b065b34cd8d806402f81ac6c8fc6c35a5900078b2`  
		Last Modified: Tue, 01 Jul 2025 05:53:49 GMT  
		Size: 200.9 MB (200864051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:647c843711afc163c783c0712d20d68c72b12035ce8e4838dfe0437ca0755b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b869c16bd3ad98c33fe9a5620313d04fa5315048e4d6a02ebdc34dc188300d6`

```dockerfile
```

-	Layers:
	-	`sha256:22839f67ae69cd8b5450dc94985dc09c61f099e68ffd7346f0e8165aefb16df9`  
		Last Modified: Tue, 01 Jul 2025 05:53:19 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:30961b78a9455044cdeebd8e41454f7826ae0890d1ecc0e442c2261047955a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214495629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7616f113838f66551152abbaa7e78bb1b6290da0165f1e95a33db5ee79db4ecd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a384e57dc162d271c967993ad51c536042f8fa44021c63d2f1e1451d01d3c`  
		Last Modified: Tue, 01 Jul 2025 09:03:37 GMT  
		Size: 49.6 MB (49556735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee7d20d2503756c5a0cea91dd771363af7976637e4c7611f6483e765d74e31`  
		Last Modified: Tue, 01 Jul 2025 09:03:29 GMT  
		Size: 1.2 MB (1224878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e97106d5b222a68acbdae51583cfc0a75ba53e01f57bdb345f142a5f9ff64a0`  
		Last Modified: Tue, 01 Jul 2025 09:12:28 GMT  
		Size: 139.8 MB (139775240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:b69fd6a56114da5a99b236eb4b08821c7967d3ccd4d6bcc8522d997ea6540db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedf7f483396412ba0b566c8f047fd67ece80adfa19c540b1fc89e776393bc63`

```dockerfile
```

-	Layers:
	-	`sha256:d1f48b8093c2678f6877cdd055da43ced65e56e5d5f64328d9b3b5774e406c40`  
		Last Modified: Tue, 01 Jul 2025 11:53:22 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:6c4ba78803afed3f4f89c2e1cb5f7eeefc11bdf7621520a532cee3f394436549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284486186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ec929ca46b8fa33558ef4129121da8c2572970244cc227a5328014eee31ce3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69c2715daafc240c33dedb398493c36f5697dc53cc8c9ef8c66db70503b768c`  
		Last Modified: Tue, 01 Jul 2025 06:59:17 GMT  
		Size: 54.7 MB (54695649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f06f85123f3f957451b79d3bc63ba1b3045a3fcb3d921481b36f1ae11892087`  
		Last Modified: Tue, 01 Jul 2025 06:59:00 GMT  
		Size: 1.5 MB (1491204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f53f4a2356e25368725c1421c7511b559baf5914ac33118f66a54e4505a229`  
		Last Modified: Tue, 01 Jul 2025 08:27:52 GMT  
		Size: 200.2 MB (200221623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:a98ad7aa9bce661ceb25b3b6342582bbdfda5ee7de83b719c329d36a1b1e8fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804bc826bf83e4d5dc041066aa7c1725dec624ca6cfc78a1f6cd23b92535c2c7`

```dockerfile
```

-	Layers:
	-	`sha256:736f01326d3c430d8d8fc479826197a5abcac1b1c6e61191cee9620f5d06b45a`  
		Last Modified: Tue, 01 Jul 2025 08:53:22 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:5675e2e8e963024328dedc075af5eec0824f1f0c9728ef0f0c673ea098efac79
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
$ docker pull dart@sha256:2fdf4ee8914e661e714243fecef04625354febc8f527e7194baa78f23566bd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285802648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383978bad3d34de5e093cc36e7e574bb41eef7f6b53d898789b0fe4dd75c6a57`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758698419310856f0fdd07e1d59d6227640490bfa69978d7e37c9bb5d19697c2`  
		Last Modified: Tue, 01 Jul 2025 02:26:27 GMT  
		Size: 54.9 MB (54920852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e01113bdd1f9cd91dddfd1b2af92a0a37607fca21f83c0098ece68db8f3cc2`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 1.8 MB (1787570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c98b4987321144ec38891b065b34cd8d806402f81ac6c8fc6c35a5900078b2`  
		Last Modified: Tue, 01 Jul 2025 05:53:49 GMT  
		Size: 200.9 MB (200864051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:647c843711afc163c783c0712d20d68c72b12035ce8e4838dfe0437ca0755b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b869c16bd3ad98c33fe9a5620313d04fa5315048e4d6a02ebdc34dc188300d6`

```dockerfile
```

-	Layers:
	-	`sha256:22839f67ae69cd8b5450dc94985dc09c61f099e68ffd7346f0e8165aefb16df9`  
		Last Modified: Tue, 01 Jul 2025 05:53:19 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:30961b78a9455044cdeebd8e41454f7826ae0890d1ecc0e442c2261047955a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214495629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7616f113838f66551152abbaa7e78bb1b6290da0165f1e95a33db5ee79db4ecd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a384e57dc162d271c967993ad51c536042f8fa44021c63d2f1e1451d01d3c`  
		Last Modified: Tue, 01 Jul 2025 09:03:37 GMT  
		Size: 49.6 MB (49556735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee7d20d2503756c5a0cea91dd771363af7976637e4c7611f6483e765d74e31`  
		Last Modified: Tue, 01 Jul 2025 09:03:29 GMT  
		Size: 1.2 MB (1224878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e97106d5b222a68acbdae51583cfc0a75ba53e01f57bdb345f142a5f9ff64a0`  
		Last Modified: Tue, 01 Jul 2025 09:12:28 GMT  
		Size: 139.8 MB (139775240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b69fd6a56114da5a99b236eb4b08821c7967d3ccd4d6bcc8522d997ea6540db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedf7f483396412ba0b566c8f047fd67ece80adfa19c540b1fc89e776393bc63`

```dockerfile
```

-	Layers:
	-	`sha256:d1f48b8093c2678f6877cdd055da43ced65e56e5d5f64328d9b3b5774e406c40`  
		Last Modified: Tue, 01 Jul 2025 11:53:22 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:6c4ba78803afed3f4f89c2e1cb5f7eeefc11bdf7621520a532cee3f394436549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284486186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ec929ca46b8fa33558ef4129121da8c2572970244cc227a5328014eee31ce3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69c2715daafc240c33dedb398493c36f5697dc53cc8c9ef8c66db70503b768c`  
		Last Modified: Tue, 01 Jul 2025 06:59:17 GMT  
		Size: 54.7 MB (54695649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f06f85123f3f957451b79d3bc63ba1b3045a3fcb3d921481b36f1ae11892087`  
		Last Modified: Tue, 01 Jul 2025 06:59:00 GMT  
		Size: 1.5 MB (1491204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f53f4a2356e25368725c1421c7511b559baf5914ac33118f66a54e4505a229`  
		Last Modified: Tue, 01 Jul 2025 08:27:52 GMT  
		Size: 200.2 MB (200221623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a98ad7aa9bce661ceb25b3b6342582bbdfda5ee7de83b719c329d36a1b1e8fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804bc826bf83e4d5dc041066aa7c1725dec624ca6cfc78a1f6cd23b92535c2c7`

```dockerfile
```

-	Layers:
	-	`sha256:736f01326d3c430d8d8fc479826197a5abcac1b1c6e61191cee9620f5d06b45a`  
		Last Modified: Tue, 01 Jul 2025 08:53:22 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json
