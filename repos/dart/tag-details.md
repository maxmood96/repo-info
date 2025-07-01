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
$ docker pull dart@sha256:5db6c329bc7499fe76a67106dc32269f86c5f014f5ac7e6d5860fa6ee5aa3587
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
$ docker pull dart@sha256:0d6c4e08a0df4341ab8754418d43a6df4ebc2059579b9e8ddfb040402f5934b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214490678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9f47c2d9e5ee2c85ba702dfc77bb80846b41ea8f03e2f489a474ae7802669`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c13cfb1e457e1db034d3d8dbb41e1ac4441b9265cad815d20d2e18f2fd92b7`  
		Last Modified: Wed, 11 Jun 2025 05:53:42 GMT  
		Size: 49.6 MB (49554691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8913a34ef1b12f14e3def3cfea96e72e91804657555a02d6912c14cfedaf`  
		Last Modified: Wed, 11 Jun 2025 05:12:21 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd53944abf9eecaddc2148601ab23afdaa2b69bb36202fc947bdf17be53bb785`  
		Last Modified: Wed, 11 Jun 2025 05:53:46 GMT  
		Size: 139.8 MB (139775267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:677a33b1639693ad7c00593f0649db746166227b73fc3c02d46ef6f4b91486e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b223d4f7e131718996fe85a74df9696702f4b6303954e3c850d7bef071f99`

```dockerfile
```

-	Layers:
	-	`sha256:187ce532a4b8f6cccdf13506fddd3895ff978429e3c48678d152c510ab6ad705`  
		Last Modified: Wed, 11 Jun 2025 05:53:21 GMT  
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
$ docker pull dart@sha256:5db6c329bc7499fe76a67106dc32269f86c5f014f5ac7e6d5860fa6ee5aa3587
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
$ docker pull dart@sha256:0d6c4e08a0df4341ab8754418d43a6df4ebc2059579b9e8ddfb040402f5934b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214490678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9f47c2d9e5ee2c85ba702dfc77bb80846b41ea8f03e2f489a474ae7802669`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c13cfb1e457e1db034d3d8dbb41e1ac4441b9265cad815d20d2e18f2fd92b7`  
		Last Modified: Wed, 11 Jun 2025 05:53:42 GMT  
		Size: 49.6 MB (49554691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8913a34ef1b12f14e3def3cfea96e72e91804657555a02d6912c14cfedaf`  
		Last Modified: Wed, 11 Jun 2025 05:12:21 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd53944abf9eecaddc2148601ab23afdaa2b69bb36202fc947bdf17be53bb785`  
		Last Modified: Wed, 11 Jun 2025 05:53:46 GMT  
		Size: 139.8 MB (139775267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:677a33b1639693ad7c00593f0649db746166227b73fc3c02d46ef6f4b91486e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b223d4f7e131718996fe85a74df9696702f4b6303954e3c850d7bef071f99`

```dockerfile
```

-	Layers:
	-	`sha256:187ce532a4b8f6cccdf13506fddd3895ff978429e3c48678d152c510ab6ad705`  
		Last Modified: Wed, 11 Jun 2025 05:53:21 GMT  
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
$ docker pull dart@sha256:5db6c329bc7499fe76a67106dc32269f86c5f014f5ac7e6d5860fa6ee5aa3587
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
$ docker pull dart@sha256:0d6c4e08a0df4341ab8754418d43a6df4ebc2059579b9e8ddfb040402f5934b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214490678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9f47c2d9e5ee2c85ba702dfc77bb80846b41ea8f03e2f489a474ae7802669`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c13cfb1e457e1db034d3d8dbb41e1ac4441b9265cad815d20d2e18f2fd92b7`  
		Last Modified: Wed, 11 Jun 2025 05:53:42 GMT  
		Size: 49.6 MB (49554691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8913a34ef1b12f14e3def3cfea96e72e91804657555a02d6912c14cfedaf`  
		Last Modified: Wed, 11 Jun 2025 05:12:21 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd53944abf9eecaddc2148601ab23afdaa2b69bb36202fc947bdf17be53bb785`  
		Last Modified: Wed, 11 Jun 2025 05:53:46 GMT  
		Size: 139.8 MB (139775267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8` - unknown; unknown

```console
$ docker pull dart@sha256:677a33b1639693ad7c00593f0649db746166227b73fc3c02d46ef6f4b91486e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b223d4f7e131718996fe85a74df9696702f4b6303954e3c850d7bef071f99`

```dockerfile
```

-	Layers:
	-	`sha256:187ce532a4b8f6cccdf13506fddd3895ff978429e3c48678d152c510ab6ad705`  
		Last Modified: Wed, 11 Jun 2025 05:53:21 GMT  
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
$ docker pull dart@sha256:5db6c329bc7499fe76a67106dc32269f86c5f014f5ac7e6d5860fa6ee5aa3587
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
$ docker pull dart@sha256:0d6c4e08a0df4341ab8754418d43a6df4ebc2059579b9e8ddfb040402f5934b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214490678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9f47c2d9e5ee2c85ba702dfc77bb80846b41ea8f03e2f489a474ae7802669`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c13cfb1e457e1db034d3d8dbb41e1ac4441b9265cad815d20d2e18f2fd92b7`  
		Last Modified: Wed, 11 Jun 2025 05:53:42 GMT  
		Size: 49.6 MB (49554691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8913a34ef1b12f14e3def3cfea96e72e91804657555a02d6912c14cfedaf`  
		Last Modified: Wed, 11 Jun 2025 05:12:21 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd53944abf9eecaddc2148601ab23afdaa2b69bb36202fc947bdf17be53bb785`  
		Last Modified: Wed, 11 Jun 2025 05:53:46 GMT  
		Size: 139.8 MB (139775267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:677a33b1639693ad7c00593f0649db746166227b73fc3c02d46ef6f4b91486e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b223d4f7e131718996fe85a74df9696702f4b6303954e3c850d7bef071f99`

```dockerfile
```

-	Layers:
	-	`sha256:187ce532a4b8f6cccdf13506fddd3895ff978429e3c48678d152c510ab6ad705`  
		Last Modified: Wed, 11 Jun 2025 05:53:21 GMT  
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
$ docker pull dart@sha256:5db6c329bc7499fe76a67106dc32269f86c5f014f5ac7e6d5860fa6ee5aa3587
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
$ docker pull dart@sha256:0d6c4e08a0df4341ab8754418d43a6df4ebc2059579b9e8ddfb040402f5934b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214490678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9f47c2d9e5ee2c85ba702dfc77bb80846b41ea8f03e2f489a474ae7802669`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c13cfb1e457e1db034d3d8dbb41e1ac4441b9265cad815d20d2e18f2fd92b7`  
		Last Modified: Wed, 11 Jun 2025 05:53:42 GMT  
		Size: 49.6 MB (49554691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8913a34ef1b12f14e3def3cfea96e72e91804657555a02d6912c14cfedaf`  
		Last Modified: Wed, 11 Jun 2025 05:12:21 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd53944abf9eecaddc2148601ab23afdaa2b69bb36202fc947bdf17be53bb785`  
		Last Modified: Wed, 11 Jun 2025 05:53:46 GMT  
		Size: 139.8 MB (139775267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.1` - unknown; unknown

```console
$ docker pull dart@sha256:677a33b1639693ad7c00593f0649db746166227b73fc3c02d46ef6f4b91486e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b223d4f7e131718996fe85a74df9696702f4b6303954e3c850d7bef071f99`

```dockerfile
```

-	Layers:
	-	`sha256:187ce532a4b8f6cccdf13506fddd3895ff978429e3c48678d152c510ab6ad705`  
		Last Modified: Wed, 11 Jun 2025 05:53:21 GMT  
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
$ docker pull dart@sha256:5db6c329bc7499fe76a67106dc32269f86c5f014f5ac7e6d5860fa6ee5aa3587
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
$ docker pull dart@sha256:0d6c4e08a0df4341ab8754418d43a6df4ebc2059579b9e8ddfb040402f5934b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214490678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9f47c2d9e5ee2c85ba702dfc77bb80846b41ea8f03e2f489a474ae7802669`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c13cfb1e457e1db034d3d8dbb41e1ac4441b9265cad815d20d2e18f2fd92b7`  
		Last Modified: Wed, 11 Jun 2025 05:53:42 GMT  
		Size: 49.6 MB (49554691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8913a34ef1b12f14e3def3cfea96e72e91804657555a02d6912c14cfedaf`  
		Last Modified: Wed, 11 Jun 2025 05:12:21 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd53944abf9eecaddc2148601ab23afdaa2b69bb36202fc947bdf17be53bb785`  
		Last Modified: Wed, 11 Jun 2025 05:53:46 GMT  
		Size: 139.8 MB (139775267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:677a33b1639693ad7c00593f0649db746166227b73fc3c02d46ef6f4b91486e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b223d4f7e131718996fe85a74df9696702f4b6303954e3c850d7bef071f99`

```dockerfile
```

-	Layers:
	-	`sha256:187ce532a4b8f6cccdf13506fddd3895ff978429e3c48678d152c510ab6ad705`  
		Last Modified: Wed, 11 Jun 2025 05:53:21 GMT  
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
$ docker pull dart@sha256:2c7d392d8901f8cfb23988638cbabe645c155da9c4df973e3cbc0e5723a9b0e4
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
$ docker pull dart@sha256:3236e1e7e8764b0e7050ed16d9dea57a1df669e9c534970efd538382ebd1b3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228495385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed524c81192289769ee334fb09313a0c46a73de3943d80e756157a292c47bab0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
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
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91b5445b5cd74396ae398266097364c0789e065f5d63837e18fdabb4c59b0cb`  
		Last Modified: Fri, 20 Jun 2025 18:55:42 GMT  
		Size: 49.6 MB (49559425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffb13dcfc43925f43218d3c69a9e1dae1baa9b3a09f39e988de50ca0c874616`  
		Last Modified: Fri, 20 Jun 2025 18:55:34 GMT  
		Size: 1.2 MB (1224883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cfdf86d4d8c1745e6df8271c6306284b455ce14ac13427517532ada8018659`  
		Last Modified: Fri, 20 Jun 2025 20:53:53 GMT  
		Size: 153.8 MB (153772301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-196.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:bbab9c42787843b1f3691f9b8c5f0d4859b869edcd730cb8bebd407c92b46944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6c4a847f94d1882895eefa04010a6f3a0341dda5fdc05157e59826b29523d7`

```dockerfile
```

-	Layers:
	-	`sha256:bc177005bdd640ce7a1ee92cb4d47b49e785f38b00cc7a02f604a2d930fc3ebf`  
		Last Modified: Fri, 20 Jun 2025 20:53:31 GMT  
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
$ docker pull dart@sha256:2c7d392d8901f8cfb23988638cbabe645c155da9c4df973e3cbc0e5723a9b0e4
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
$ docker pull dart@sha256:3236e1e7e8764b0e7050ed16d9dea57a1df669e9c534970efd538382ebd1b3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228495385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed524c81192289769ee334fb09313a0c46a73de3943d80e756157a292c47bab0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
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
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91b5445b5cd74396ae398266097364c0789e065f5d63837e18fdabb4c59b0cb`  
		Last Modified: Fri, 20 Jun 2025 18:55:42 GMT  
		Size: 49.6 MB (49559425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffb13dcfc43925f43218d3c69a9e1dae1baa9b3a09f39e988de50ca0c874616`  
		Last Modified: Fri, 20 Jun 2025 18:55:34 GMT  
		Size: 1.2 MB (1224883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cfdf86d4d8c1745e6df8271c6306284b455ce14ac13427517532ada8018659`  
		Last Modified: Fri, 20 Jun 2025 20:53:53 GMT  
		Size: 153.8 MB (153772301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-196.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:bbab9c42787843b1f3691f9b8c5f0d4859b869edcd730cb8bebd407c92b46944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6c4a847f94d1882895eefa04010a6f3a0341dda5fdc05157e59826b29523d7`

```dockerfile
```

-	Layers:
	-	`sha256:bc177005bdd640ce7a1ee92cb4d47b49e785f38b00cc7a02f604a2d930fc3ebf`  
		Last Modified: Fri, 20 Jun 2025 20:53:31 GMT  
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
$ docker pull dart@sha256:2c7d392d8901f8cfb23988638cbabe645c155da9c4df973e3cbc0e5723a9b0e4
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
$ docker pull dart@sha256:3236e1e7e8764b0e7050ed16d9dea57a1df669e9c534970efd538382ebd1b3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228495385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed524c81192289769ee334fb09313a0c46a73de3943d80e756157a292c47bab0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
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
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91b5445b5cd74396ae398266097364c0789e065f5d63837e18fdabb4c59b0cb`  
		Last Modified: Fri, 20 Jun 2025 18:55:42 GMT  
		Size: 49.6 MB (49559425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffb13dcfc43925f43218d3c69a9e1dae1baa9b3a09f39e988de50ca0c874616`  
		Last Modified: Fri, 20 Jun 2025 18:55:34 GMT  
		Size: 1.2 MB (1224883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cfdf86d4d8c1745e6df8271c6306284b455ce14ac13427517532ada8018659`  
		Last Modified: Fri, 20 Jun 2025 20:53:53 GMT  
		Size: 153.8 MB (153772301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:bbab9c42787843b1f3691f9b8c5f0d4859b869edcd730cb8bebd407c92b46944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6c4a847f94d1882895eefa04010a6f3a0341dda5fdc05157e59826b29523d7`

```dockerfile
```

-	Layers:
	-	`sha256:bc177005bdd640ce7a1ee92cb4d47b49e785f38b00cc7a02f604a2d930fc3ebf`  
		Last Modified: Fri, 20 Jun 2025 20:53:31 GMT  
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
$ docker pull dart@sha256:2c7d392d8901f8cfb23988638cbabe645c155da9c4df973e3cbc0e5723a9b0e4
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
$ docker pull dart@sha256:3236e1e7e8764b0e7050ed16d9dea57a1df669e9c534970efd538382ebd1b3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228495385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed524c81192289769ee334fb09313a0c46a73de3943d80e756157a292c47bab0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
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
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91b5445b5cd74396ae398266097364c0789e065f5d63837e18fdabb4c59b0cb`  
		Last Modified: Fri, 20 Jun 2025 18:55:42 GMT  
		Size: 49.6 MB (49559425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffb13dcfc43925f43218d3c69a9e1dae1baa9b3a09f39e988de50ca0c874616`  
		Last Modified: Fri, 20 Jun 2025 18:55:34 GMT  
		Size: 1.2 MB (1224883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cfdf86d4d8c1745e6df8271c6306284b455ce14ac13427517532ada8018659`  
		Last Modified: Fri, 20 Jun 2025 20:53:53 GMT  
		Size: 153.8 MB (153772301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:bbab9c42787843b1f3691f9b8c5f0d4859b869edcd730cb8bebd407c92b46944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6c4a847f94d1882895eefa04010a6f3a0341dda5fdc05157e59826b29523d7`

```dockerfile
```

-	Layers:
	-	`sha256:bc177005bdd640ce7a1ee92cb4d47b49e785f38b00cc7a02f604a2d930fc3ebf`  
		Last Modified: Fri, 20 Jun 2025 20:53:31 GMT  
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
$ docker pull dart@sha256:5db6c329bc7499fe76a67106dc32269f86c5f014f5ac7e6d5860fa6ee5aa3587
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
$ docker pull dart@sha256:0d6c4e08a0df4341ab8754418d43a6df4ebc2059579b9e8ddfb040402f5934b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214490678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9f47c2d9e5ee2c85ba702dfc77bb80846b41ea8f03e2f489a474ae7802669`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c13cfb1e457e1db034d3d8dbb41e1ac4441b9265cad815d20d2e18f2fd92b7`  
		Last Modified: Wed, 11 Jun 2025 05:53:42 GMT  
		Size: 49.6 MB (49554691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8913a34ef1b12f14e3def3cfea96e72e91804657555a02d6912c14cfedaf`  
		Last Modified: Wed, 11 Jun 2025 05:12:21 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd53944abf9eecaddc2148601ab23afdaa2b69bb36202fc947bdf17be53bb785`  
		Last Modified: Wed, 11 Jun 2025 05:53:46 GMT  
		Size: 139.8 MB (139775267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:677a33b1639693ad7c00593f0649db746166227b73fc3c02d46ef6f4b91486e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b223d4f7e131718996fe85a74df9696702f4b6303954e3c850d7bef071f99`

```dockerfile
```

-	Layers:
	-	`sha256:187ce532a4b8f6cccdf13506fddd3895ff978429e3c48678d152c510ab6ad705`  
		Last Modified: Wed, 11 Jun 2025 05:53:21 GMT  
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
$ docker pull dart@sha256:5db6c329bc7499fe76a67106dc32269f86c5f014f5ac7e6d5860fa6ee5aa3587
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
$ docker pull dart@sha256:0d6c4e08a0df4341ab8754418d43a6df4ebc2059579b9e8ddfb040402f5934b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214490678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9f47c2d9e5ee2c85ba702dfc77bb80846b41ea8f03e2f489a474ae7802669`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c13cfb1e457e1db034d3d8dbb41e1ac4441b9265cad815d20d2e18f2fd92b7`  
		Last Modified: Wed, 11 Jun 2025 05:53:42 GMT  
		Size: 49.6 MB (49554691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8913a34ef1b12f14e3def3cfea96e72e91804657555a02d6912c14cfedaf`  
		Last Modified: Wed, 11 Jun 2025 05:12:21 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd53944abf9eecaddc2148601ab23afdaa2b69bb36202fc947bdf17be53bb785`  
		Last Modified: Wed, 11 Jun 2025 05:53:46 GMT  
		Size: 139.8 MB (139775267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:677a33b1639693ad7c00593f0649db746166227b73fc3c02d46ef6f4b91486e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b223d4f7e131718996fe85a74df9696702f4b6303954e3c850d7bef071f99`

```dockerfile
```

-	Layers:
	-	`sha256:187ce532a4b8f6cccdf13506fddd3895ff978429e3c48678d152c510ab6ad705`  
		Last Modified: Wed, 11 Jun 2025 05:53:21 GMT  
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
$ docker pull dart@sha256:5db6c329bc7499fe76a67106dc32269f86c5f014f5ac7e6d5860fa6ee5aa3587
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
$ docker pull dart@sha256:0d6c4e08a0df4341ab8754418d43a6df4ebc2059579b9e8ddfb040402f5934b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214490678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9f47c2d9e5ee2c85ba702dfc77bb80846b41ea8f03e2f489a474ae7802669`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c13cfb1e457e1db034d3d8dbb41e1ac4441b9265cad815d20d2e18f2fd92b7`  
		Last Modified: Wed, 11 Jun 2025 05:53:42 GMT  
		Size: 49.6 MB (49554691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8913a34ef1b12f14e3def3cfea96e72e91804657555a02d6912c14cfedaf`  
		Last Modified: Wed, 11 Jun 2025 05:12:21 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd53944abf9eecaddc2148601ab23afdaa2b69bb36202fc947bdf17be53bb785`  
		Last Modified: Wed, 11 Jun 2025 05:53:46 GMT  
		Size: 139.8 MB (139775267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:677a33b1639693ad7c00593f0649db746166227b73fc3c02d46ef6f4b91486e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b223d4f7e131718996fe85a74df9696702f4b6303954e3c850d7bef071f99`

```dockerfile
```

-	Layers:
	-	`sha256:187ce532a4b8f6cccdf13506fddd3895ff978429e3c48678d152c510ab6ad705`  
		Last Modified: Wed, 11 Jun 2025 05:53:21 GMT  
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
$ docker pull dart@sha256:5db6c329bc7499fe76a67106dc32269f86c5f014f5ac7e6d5860fa6ee5aa3587
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
$ docker pull dart@sha256:0d6c4e08a0df4341ab8754418d43a6df4ebc2059579b9e8ddfb040402f5934b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214490678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9f47c2d9e5ee2c85ba702dfc77bb80846b41ea8f03e2f489a474ae7802669`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c13cfb1e457e1db034d3d8dbb41e1ac4441b9265cad815d20d2e18f2fd92b7`  
		Last Modified: Wed, 11 Jun 2025 05:53:42 GMT  
		Size: 49.6 MB (49554691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8913a34ef1b12f14e3def3cfea96e72e91804657555a02d6912c14cfedaf`  
		Last Modified: Wed, 11 Jun 2025 05:12:21 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd53944abf9eecaddc2148601ab23afdaa2b69bb36202fc947bdf17be53bb785`  
		Last Modified: Wed, 11 Jun 2025 05:53:46 GMT  
		Size: 139.8 MB (139775267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:677a33b1639693ad7c00593f0649db746166227b73fc3c02d46ef6f4b91486e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b223d4f7e131718996fe85a74df9696702f4b6303954e3c850d7bef071f99`

```dockerfile
```

-	Layers:
	-	`sha256:187ce532a4b8f6cccdf13506fddd3895ff978429e3c48678d152c510ab6ad705`  
		Last Modified: Wed, 11 Jun 2025 05:53:21 GMT  
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
