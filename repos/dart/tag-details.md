<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.6`](#dart36)
-	[`dart:3.6-sdk`](#dart36-sdk)
-	[`dart:3.6.1`](#dart361)
-	[`dart:3.6.1-sdk`](#dart361-sdk)
-	[`dart:3.7.0-209.1.beta`](#dart370-2091beta)
-	[`dart:3.7.0-209.1.beta-sdk`](#dart370-2091beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:032365a0d5255fe25674d49ab62cca5967e7f68d6d9c9bec6fd5f431daec9c30
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
$ docker pull dart@sha256:54ff82f6115ca4dd37d996ec8e4a147f1bfad3d13c6727d41fa72dbd6be93014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312109862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f12c4e4e00c168ba5b03d030436bf02b42196e3c59431563b45a2b4ac26d69`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc7cd33f899e4916e106343a4113582014e4f881bf6450fcfd9895b97144128`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 54.9 MB (54906759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76dc3d94143d68fa2c1275b3b5818e40ff1e814c8dbd437bab043c0a86d53a5`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 1.8 MB (1796901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558a6aaaa919082dfa0c6a496de4b31e2b411ac34c5dc44c6daa7daa5f1a1e12`  
		Last Modified: Tue, 04 Feb 2025 04:39:01 GMT  
		Size: 227.2 MB (227193867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:b52d4615255da33008bad8c9435f8b75cd6a77cd7a2b16354b2607fd8326bc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9880eca97e150d3af6afd4138bdecf47c64f17251078d7ee2f3e9605d405f4`

```dockerfile
```

-	Layers:
	-	`sha256:cf60c365df752c55eeebfca95b9ed8bf6f897ab517f78568cb645091d664e6b4`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:da2f3a7a5c08d691552eb23f673dfc18a4b04be147427d571f29acfc6a4e5729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210395961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f297840472ff7b5b8a16c48469f8a8a5d157ef34ff1832b4cd13e73bfb1d06`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1b2dab5a73d378cc31835ab53f09fb017cb86b517a3b983911442a2d031149`  
		Last Modified: Tue, 04 Feb 2025 10:49:05 GMT  
		Size: 49.6 MB (49561346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef7554d5be4301c1388ee54c011ee6ea7e854972805f5d3e2ab4c2aa4c995d`  
		Last Modified: Tue, 04 Feb 2025 10:49:03 GMT  
		Size: 1.2 MB (1221672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756485da8bc62b90f72a0888b60302d5dd366a23d1991fa57fa36696efe1eba7`  
		Last Modified: Tue, 04 Feb 2025 10:49:07 GMT  
		Size: 135.7 MB (135698375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:4cf6c57feb50a6a416e26b63c0c1f359b00641479c3314eed783d9300d14c7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7b07ad7d4ff87adacda784c76a6cecf85b72fa57f5e03be879be6d4f009294`

```dockerfile
```

-	Layers:
	-	`sha256:1922626f788f7f2f113503744e0ce772858422592a4af70e482e87c4b0fd19e7`  
		Last Modified: Tue, 04 Feb 2025 10:49:03 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:a0c55f1753b9ff278bd0ee678df370d694ea10368b1d7f6d541db2f0ac204e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310566943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27acde1cc697fa5419a877250603d4105d19c22e42fe8ef1800e07408a91b42`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126af0939b0f0fe80d45e16234ab959ce4b7569c531cbe68fecd59ad47ae146`  
		Last Modified: Tue, 04 Feb 2025 09:15:07 GMT  
		Size: 54.7 MB (54678176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76895c45ded445277d80dfcaee0f604a00263996e451eac21374f668be3a475`  
		Last Modified: Tue, 04 Feb 2025 09:15:05 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad043eee0fb851a491b72173522e3bbc03336c27dad17069a3e22e2820dc2f4`  
		Last Modified: Tue, 04 Feb 2025 09:15:10 GMT  
		Size: 226.4 MB (226359825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:11984afe369c09c981cee162fbcce42137610edc1ebce78d802cd27e98e90f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ed972963d0876d62e4a5ead5a164642912ce5004180aa897645637dea888f6`

```dockerfile
```

-	Layers:
	-	`sha256:a18cf7749b6b46e33600329e8fceaf8dce378e5975fe8195e32a7d3562738cf0`  
		Last Modified: Tue, 04 Feb 2025 09:15:05 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:032365a0d5255fe25674d49ab62cca5967e7f68d6d9c9bec6fd5f431daec9c30
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
$ docker pull dart@sha256:54ff82f6115ca4dd37d996ec8e4a147f1bfad3d13c6727d41fa72dbd6be93014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312109862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f12c4e4e00c168ba5b03d030436bf02b42196e3c59431563b45a2b4ac26d69`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc7cd33f899e4916e106343a4113582014e4f881bf6450fcfd9895b97144128`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 54.9 MB (54906759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76dc3d94143d68fa2c1275b3b5818e40ff1e814c8dbd437bab043c0a86d53a5`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 1.8 MB (1796901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558a6aaaa919082dfa0c6a496de4b31e2b411ac34c5dc44c6daa7daa5f1a1e12`  
		Last Modified: Tue, 04 Feb 2025 04:39:01 GMT  
		Size: 227.2 MB (227193867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b52d4615255da33008bad8c9435f8b75cd6a77cd7a2b16354b2607fd8326bc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9880eca97e150d3af6afd4138bdecf47c64f17251078d7ee2f3e9605d405f4`

```dockerfile
```

-	Layers:
	-	`sha256:cf60c365df752c55eeebfca95b9ed8bf6f897ab517f78568cb645091d664e6b4`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:da2f3a7a5c08d691552eb23f673dfc18a4b04be147427d571f29acfc6a4e5729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210395961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f297840472ff7b5b8a16c48469f8a8a5d157ef34ff1832b4cd13e73bfb1d06`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1b2dab5a73d378cc31835ab53f09fb017cb86b517a3b983911442a2d031149`  
		Last Modified: Tue, 04 Feb 2025 10:49:05 GMT  
		Size: 49.6 MB (49561346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef7554d5be4301c1388ee54c011ee6ea7e854972805f5d3e2ab4c2aa4c995d`  
		Last Modified: Tue, 04 Feb 2025 10:49:03 GMT  
		Size: 1.2 MB (1221672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756485da8bc62b90f72a0888b60302d5dd366a23d1991fa57fa36696efe1eba7`  
		Last Modified: Tue, 04 Feb 2025 10:49:07 GMT  
		Size: 135.7 MB (135698375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4cf6c57feb50a6a416e26b63c0c1f359b00641479c3314eed783d9300d14c7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7b07ad7d4ff87adacda784c76a6cecf85b72fa57f5e03be879be6d4f009294`

```dockerfile
```

-	Layers:
	-	`sha256:1922626f788f7f2f113503744e0ce772858422592a4af70e482e87c4b0fd19e7`  
		Last Modified: Tue, 04 Feb 2025 10:49:03 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:a0c55f1753b9ff278bd0ee678df370d694ea10368b1d7f6d541db2f0ac204e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310566943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27acde1cc697fa5419a877250603d4105d19c22e42fe8ef1800e07408a91b42`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126af0939b0f0fe80d45e16234ab959ce4b7569c531cbe68fecd59ad47ae146`  
		Last Modified: Tue, 04 Feb 2025 09:15:07 GMT  
		Size: 54.7 MB (54678176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76895c45ded445277d80dfcaee0f604a00263996e451eac21374f668be3a475`  
		Last Modified: Tue, 04 Feb 2025 09:15:05 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad043eee0fb851a491b72173522e3bbc03336c27dad17069a3e22e2820dc2f4`  
		Last Modified: Tue, 04 Feb 2025 09:15:10 GMT  
		Size: 226.4 MB (226359825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:11984afe369c09c981cee162fbcce42137610edc1ebce78d802cd27e98e90f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ed972963d0876d62e4a5ead5a164642912ce5004180aa897645637dea888f6`

```dockerfile
```

-	Layers:
	-	`sha256:a18cf7749b6b46e33600329e8fceaf8dce378e5975fe8195e32a7d3562738cf0`  
		Last Modified: Tue, 04 Feb 2025 09:15:05 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.6`

```console
$ docker pull dart@sha256:032365a0d5255fe25674d49ab62cca5967e7f68d6d9c9bec6fd5f431daec9c30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.6` - linux; amd64

```console
$ docker pull dart@sha256:54ff82f6115ca4dd37d996ec8e4a147f1bfad3d13c6727d41fa72dbd6be93014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312109862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f12c4e4e00c168ba5b03d030436bf02b42196e3c59431563b45a2b4ac26d69`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc7cd33f899e4916e106343a4113582014e4f881bf6450fcfd9895b97144128`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 54.9 MB (54906759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76dc3d94143d68fa2c1275b3b5818e40ff1e814c8dbd437bab043c0a86d53a5`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 1.8 MB (1796901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558a6aaaa919082dfa0c6a496de4b31e2b411ac34c5dc44c6daa7daa5f1a1e12`  
		Last Modified: Tue, 04 Feb 2025 04:39:01 GMT  
		Size: 227.2 MB (227193867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6` - unknown; unknown

```console
$ docker pull dart@sha256:b52d4615255da33008bad8c9435f8b75cd6a77cd7a2b16354b2607fd8326bc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9880eca97e150d3af6afd4138bdecf47c64f17251078d7ee2f3e9605d405f4`

```dockerfile
```

-	Layers:
	-	`sha256:cf60c365df752c55eeebfca95b9ed8bf6f897ab517f78568cb645091d664e6b4`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.6` - linux; arm variant v7

```console
$ docker pull dart@sha256:da2f3a7a5c08d691552eb23f673dfc18a4b04be147427d571f29acfc6a4e5729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210395961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f297840472ff7b5b8a16c48469f8a8a5d157ef34ff1832b4cd13e73bfb1d06`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1b2dab5a73d378cc31835ab53f09fb017cb86b517a3b983911442a2d031149`  
		Last Modified: Tue, 04 Feb 2025 10:49:05 GMT  
		Size: 49.6 MB (49561346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef7554d5be4301c1388ee54c011ee6ea7e854972805f5d3e2ab4c2aa4c995d`  
		Last Modified: Tue, 04 Feb 2025 10:49:03 GMT  
		Size: 1.2 MB (1221672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756485da8bc62b90f72a0888b60302d5dd366a23d1991fa57fa36696efe1eba7`  
		Last Modified: Tue, 04 Feb 2025 10:49:07 GMT  
		Size: 135.7 MB (135698375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6` - unknown; unknown

```console
$ docker pull dart@sha256:4cf6c57feb50a6a416e26b63c0c1f359b00641479c3314eed783d9300d14c7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7b07ad7d4ff87adacda784c76a6cecf85b72fa57f5e03be879be6d4f009294`

```dockerfile
```

-	Layers:
	-	`sha256:1922626f788f7f2f113503744e0ce772858422592a4af70e482e87c4b0fd19e7`  
		Last Modified: Tue, 04 Feb 2025 10:49:03 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.6` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:a0c55f1753b9ff278bd0ee678df370d694ea10368b1d7f6d541db2f0ac204e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310566943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27acde1cc697fa5419a877250603d4105d19c22e42fe8ef1800e07408a91b42`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126af0939b0f0fe80d45e16234ab959ce4b7569c531cbe68fecd59ad47ae146`  
		Last Modified: Tue, 04 Feb 2025 09:15:07 GMT  
		Size: 54.7 MB (54678176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76895c45ded445277d80dfcaee0f604a00263996e451eac21374f668be3a475`  
		Last Modified: Tue, 04 Feb 2025 09:15:05 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad043eee0fb851a491b72173522e3bbc03336c27dad17069a3e22e2820dc2f4`  
		Last Modified: Tue, 04 Feb 2025 09:15:10 GMT  
		Size: 226.4 MB (226359825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6` - unknown; unknown

```console
$ docker pull dart@sha256:11984afe369c09c981cee162fbcce42137610edc1ebce78d802cd27e98e90f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ed972963d0876d62e4a5ead5a164642912ce5004180aa897645637dea888f6`

```dockerfile
```

-	Layers:
	-	`sha256:a18cf7749b6b46e33600329e8fceaf8dce378e5975fe8195e32a7d3562738cf0`  
		Last Modified: Tue, 04 Feb 2025 09:15:05 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.6-sdk`

```console
$ docker pull dart@sha256:032365a0d5255fe25674d49ab62cca5967e7f68d6d9c9bec6fd5f431daec9c30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.6-sdk` - linux; amd64

```console
$ docker pull dart@sha256:54ff82f6115ca4dd37d996ec8e4a147f1bfad3d13c6727d41fa72dbd6be93014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312109862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f12c4e4e00c168ba5b03d030436bf02b42196e3c59431563b45a2b4ac26d69`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc7cd33f899e4916e106343a4113582014e4f881bf6450fcfd9895b97144128`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 54.9 MB (54906759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76dc3d94143d68fa2c1275b3b5818e40ff1e814c8dbd437bab043c0a86d53a5`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 1.8 MB (1796901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558a6aaaa919082dfa0c6a496de4b31e2b411ac34c5dc44c6daa7daa5f1a1e12`  
		Last Modified: Tue, 04 Feb 2025 04:39:01 GMT  
		Size: 227.2 MB (227193867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b52d4615255da33008bad8c9435f8b75cd6a77cd7a2b16354b2607fd8326bc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9880eca97e150d3af6afd4138bdecf47c64f17251078d7ee2f3e9605d405f4`

```dockerfile
```

-	Layers:
	-	`sha256:cf60c365df752c55eeebfca95b9ed8bf6f897ab517f78568cb645091d664e6b4`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.6-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:da2f3a7a5c08d691552eb23f673dfc18a4b04be147427d571f29acfc6a4e5729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210395961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f297840472ff7b5b8a16c48469f8a8a5d157ef34ff1832b4cd13e73bfb1d06`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1b2dab5a73d378cc31835ab53f09fb017cb86b517a3b983911442a2d031149`  
		Last Modified: Tue, 04 Feb 2025 10:49:05 GMT  
		Size: 49.6 MB (49561346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef7554d5be4301c1388ee54c011ee6ea7e854972805f5d3e2ab4c2aa4c995d`  
		Last Modified: Tue, 04 Feb 2025 10:49:03 GMT  
		Size: 1.2 MB (1221672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756485da8bc62b90f72a0888b60302d5dd366a23d1991fa57fa36696efe1eba7`  
		Last Modified: Tue, 04 Feb 2025 10:49:07 GMT  
		Size: 135.7 MB (135698375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4cf6c57feb50a6a416e26b63c0c1f359b00641479c3314eed783d9300d14c7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7b07ad7d4ff87adacda784c76a6cecf85b72fa57f5e03be879be6d4f009294`

```dockerfile
```

-	Layers:
	-	`sha256:1922626f788f7f2f113503744e0ce772858422592a4af70e482e87c4b0fd19e7`  
		Last Modified: Tue, 04 Feb 2025 10:49:03 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.6-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:a0c55f1753b9ff278bd0ee678df370d694ea10368b1d7f6d541db2f0ac204e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310566943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27acde1cc697fa5419a877250603d4105d19c22e42fe8ef1800e07408a91b42`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126af0939b0f0fe80d45e16234ab959ce4b7569c531cbe68fecd59ad47ae146`  
		Last Modified: Tue, 04 Feb 2025 09:15:07 GMT  
		Size: 54.7 MB (54678176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76895c45ded445277d80dfcaee0f604a00263996e451eac21374f668be3a475`  
		Last Modified: Tue, 04 Feb 2025 09:15:05 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad043eee0fb851a491b72173522e3bbc03336c27dad17069a3e22e2820dc2f4`  
		Last Modified: Tue, 04 Feb 2025 09:15:10 GMT  
		Size: 226.4 MB (226359825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:11984afe369c09c981cee162fbcce42137610edc1ebce78d802cd27e98e90f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ed972963d0876d62e4a5ead5a164642912ce5004180aa897645637dea888f6`

```dockerfile
```

-	Layers:
	-	`sha256:a18cf7749b6b46e33600329e8fceaf8dce378e5975fe8195e32a7d3562738cf0`  
		Last Modified: Tue, 04 Feb 2025 09:15:05 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.6.1`

```console
$ docker pull dart@sha256:032365a0d5255fe25674d49ab62cca5967e7f68d6d9c9bec6fd5f431daec9c30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.6.1` - linux; amd64

```console
$ docker pull dart@sha256:54ff82f6115ca4dd37d996ec8e4a147f1bfad3d13c6727d41fa72dbd6be93014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312109862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f12c4e4e00c168ba5b03d030436bf02b42196e3c59431563b45a2b4ac26d69`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc7cd33f899e4916e106343a4113582014e4f881bf6450fcfd9895b97144128`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 54.9 MB (54906759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76dc3d94143d68fa2c1275b3b5818e40ff1e814c8dbd437bab043c0a86d53a5`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 1.8 MB (1796901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558a6aaaa919082dfa0c6a496de4b31e2b411ac34c5dc44c6daa7daa5f1a1e12`  
		Last Modified: Tue, 04 Feb 2025 04:39:01 GMT  
		Size: 227.2 MB (227193867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6.1` - unknown; unknown

```console
$ docker pull dart@sha256:b52d4615255da33008bad8c9435f8b75cd6a77cd7a2b16354b2607fd8326bc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9880eca97e150d3af6afd4138bdecf47c64f17251078d7ee2f3e9605d405f4`

```dockerfile
```

-	Layers:
	-	`sha256:cf60c365df752c55eeebfca95b9ed8bf6f897ab517f78568cb645091d664e6b4`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.6.1` - linux; arm variant v7

```console
$ docker pull dart@sha256:da2f3a7a5c08d691552eb23f673dfc18a4b04be147427d571f29acfc6a4e5729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210395961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f297840472ff7b5b8a16c48469f8a8a5d157ef34ff1832b4cd13e73bfb1d06`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1b2dab5a73d378cc31835ab53f09fb017cb86b517a3b983911442a2d031149`  
		Last Modified: Tue, 04 Feb 2025 10:49:05 GMT  
		Size: 49.6 MB (49561346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef7554d5be4301c1388ee54c011ee6ea7e854972805f5d3e2ab4c2aa4c995d`  
		Last Modified: Tue, 04 Feb 2025 10:49:03 GMT  
		Size: 1.2 MB (1221672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756485da8bc62b90f72a0888b60302d5dd366a23d1991fa57fa36696efe1eba7`  
		Last Modified: Tue, 04 Feb 2025 10:49:07 GMT  
		Size: 135.7 MB (135698375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6.1` - unknown; unknown

```console
$ docker pull dart@sha256:4cf6c57feb50a6a416e26b63c0c1f359b00641479c3314eed783d9300d14c7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7b07ad7d4ff87adacda784c76a6cecf85b72fa57f5e03be879be6d4f009294`

```dockerfile
```

-	Layers:
	-	`sha256:1922626f788f7f2f113503744e0ce772858422592a4af70e482e87c4b0fd19e7`  
		Last Modified: Tue, 04 Feb 2025 10:49:03 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.6.1` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:a0c55f1753b9ff278bd0ee678df370d694ea10368b1d7f6d541db2f0ac204e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310566943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27acde1cc697fa5419a877250603d4105d19c22e42fe8ef1800e07408a91b42`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126af0939b0f0fe80d45e16234ab959ce4b7569c531cbe68fecd59ad47ae146`  
		Last Modified: Tue, 04 Feb 2025 09:15:07 GMT  
		Size: 54.7 MB (54678176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76895c45ded445277d80dfcaee0f604a00263996e451eac21374f668be3a475`  
		Last Modified: Tue, 04 Feb 2025 09:15:05 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad043eee0fb851a491b72173522e3bbc03336c27dad17069a3e22e2820dc2f4`  
		Last Modified: Tue, 04 Feb 2025 09:15:10 GMT  
		Size: 226.4 MB (226359825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6.1` - unknown; unknown

```console
$ docker pull dart@sha256:11984afe369c09c981cee162fbcce42137610edc1ebce78d802cd27e98e90f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ed972963d0876d62e4a5ead5a164642912ce5004180aa897645637dea888f6`

```dockerfile
```

-	Layers:
	-	`sha256:a18cf7749b6b46e33600329e8fceaf8dce378e5975fe8195e32a7d3562738cf0`  
		Last Modified: Tue, 04 Feb 2025 09:15:05 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.6.1-sdk`

```console
$ docker pull dart@sha256:032365a0d5255fe25674d49ab62cca5967e7f68d6d9c9bec6fd5f431daec9c30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.6.1-sdk` - linux; amd64

```console
$ docker pull dart@sha256:54ff82f6115ca4dd37d996ec8e4a147f1bfad3d13c6727d41fa72dbd6be93014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312109862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f12c4e4e00c168ba5b03d030436bf02b42196e3c59431563b45a2b4ac26d69`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc7cd33f899e4916e106343a4113582014e4f881bf6450fcfd9895b97144128`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 54.9 MB (54906759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76dc3d94143d68fa2c1275b3b5818e40ff1e814c8dbd437bab043c0a86d53a5`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 1.8 MB (1796901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558a6aaaa919082dfa0c6a496de4b31e2b411ac34c5dc44c6daa7daa5f1a1e12`  
		Last Modified: Tue, 04 Feb 2025 04:39:01 GMT  
		Size: 227.2 MB (227193867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b52d4615255da33008bad8c9435f8b75cd6a77cd7a2b16354b2607fd8326bc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9880eca97e150d3af6afd4138bdecf47c64f17251078d7ee2f3e9605d405f4`

```dockerfile
```

-	Layers:
	-	`sha256:cf60c365df752c55eeebfca95b9ed8bf6f897ab517f78568cb645091d664e6b4`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.6.1-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:da2f3a7a5c08d691552eb23f673dfc18a4b04be147427d571f29acfc6a4e5729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210395961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f297840472ff7b5b8a16c48469f8a8a5d157ef34ff1832b4cd13e73bfb1d06`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1b2dab5a73d378cc31835ab53f09fb017cb86b517a3b983911442a2d031149`  
		Last Modified: Tue, 04 Feb 2025 10:49:05 GMT  
		Size: 49.6 MB (49561346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef7554d5be4301c1388ee54c011ee6ea7e854972805f5d3e2ab4c2aa4c995d`  
		Last Modified: Tue, 04 Feb 2025 10:49:03 GMT  
		Size: 1.2 MB (1221672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756485da8bc62b90f72a0888b60302d5dd366a23d1991fa57fa36696efe1eba7`  
		Last Modified: Tue, 04 Feb 2025 10:49:07 GMT  
		Size: 135.7 MB (135698375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4cf6c57feb50a6a416e26b63c0c1f359b00641479c3314eed783d9300d14c7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7b07ad7d4ff87adacda784c76a6cecf85b72fa57f5e03be879be6d4f009294`

```dockerfile
```

-	Layers:
	-	`sha256:1922626f788f7f2f113503744e0ce772858422592a4af70e482e87c4b0fd19e7`  
		Last Modified: Tue, 04 Feb 2025 10:49:03 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.6.1-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:a0c55f1753b9ff278bd0ee678df370d694ea10368b1d7f6d541db2f0ac204e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310566943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27acde1cc697fa5419a877250603d4105d19c22e42fe8ef1800e07408a91b42`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126af0939b0f0fe80d45e16234ab959ce4b7569c531cbe68fecd59ad47ae146`  
		Last Modified: Tue, 04 Feb 2025 09:15:07 GMT  
		Size: 54.7 MB (54678176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76895c45ded445277d80dfcaee0f604a00263996e451eac21374f668be3a475`  
		Last Modified: Tue, 04 Feb 2025 09:15:05 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad043eee0fb851a491b72173522e3bbc03336c27dad17069a3e22e2820dc2f4`  
		Last Modified: Tue, 04 Feb 2025 09:15:10 GMT  
		Size: 226.4 MB (226359825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:11984afe369c09c981cee162fbcce42137610edc1ebce78d802cd27e98e90f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ed972963d0876d62e4a5ead5a164642912ce5004180aa897645637dea888f6`

```dockerfile
```

-	Layers:
	-	`sha256:a18cf7749b6b46e33600329e8fceaf8dce378e5975fe8195e32a7d3562738cf0`  
		Last Modified: Tue, 04 Feb 2025 09:15:05 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.7.0-209.1.beta`

```console
$ docker pull dart@sha256:191c03facd16f615f8b043ce5044da90bb0b59e2f95fae0ba4f9a431bd7872a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.7.0-209.1.beta` - linux; amd64

```console
$ docker pull dart@sha256:05284629b12bdceb0f9846be288067855be51fce03eb67a8dda35b8b53eb143e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302428689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10d5ccbf4ad47272e6174836235fcdcf10b4f736580b8670701ad6af4f53732`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3272313418c548b6c0cc7b4923ca6948a2aa3122e80ad7dba3b3b76339475b`  
		Last Modified: Tue, 04 Feb 2025 04:39:07 GMT  
		Size: 54.9 MB (54906745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bb93547bed34a7580ede8c3bd12b8004505aa2e3220206d15ab55832c0c208`  
		Last Modified: Tue, 04 Feb 2025 04:39:07 GMT  
		Size: 1.8 MB (1796910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29c09093637bf21915ea018ba813d5d9a2577be25a9465905a0ced49557932f`  
		Last Modified: Tue, 04 Feb 2025 04:39:10 GMT  
		Size: 217.5 MB (217512699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.0-209.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:3eb8c2f317cd497c5fc437a96e8bcf7dd2c47e10230d63f09fc7ff9593285e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc342c265535be797595e62ce9cef7ee4271e2059b400b720d24e22fbd115f9`

```dockerfile
```

-	Layers:
	-	`sha256:1a716bc7926b65cdc611d3cae5764c7056064019d7d3d49cabcce3d97a8a287d`  
		Last Modified: Tue, 04 Feb 2025 04:39:06 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7.0-209.1.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:d4e0395e52c2cae1cf1fd799039b7dcaf3dad424220c2e1fdbeb5d3d791ec0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.9 MB (224928443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4264477b92316c8ff78809907e27077229e47eec70e21874b5da54d5ce748f33`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8af8a5133a30e975a3b9d74bf15cc52f8d673450261b1a58fdfcd7f3a20aeb`  
		Last Modified: Tue, 04 Feb 2025 10:50:18 GMT  
		Size: 49.6 MB (49561568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17612930c2cc3b54370d8e7a9709ce77958469f4b54a2958676f7545909b77e`  
		Last Modified: Tue, 04 Feb 2025 10:50:17 GMT  
		Size: 1.2 MB (1221681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21316a5b5b0d4084df0abf17c5b0bf5d6672435763f3c2fd27a4aeb8147a6be5`  
		Last Modified: Tue, 04 Feb 2025 10:50:21 GMT  
		Size: 150.2 MB (150230626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.0-209.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:939e154100cff3d2ab12b41cdb8d198adc770a8ed76478585802d223e124841e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c17a53a5437bcc22bb8fe18a0bee266234cec83fdad76f071a6c8150ce5e0c6`

```dockerfile
```

-	Layers:
	-	`sha256:bc72fa39423d4a92a051ffbb23a6e51a7775cf8565521c793d0656b202e8c587`  
		Last Modified: Tue, 04 Feb 2025 10:50:17 GMT  
		Size: 18.0 KB (18012 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7.0-209.1.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4fe4a41963df49f4c24e5ee381239c4a1497acd3a1bd2ba59d32f817454e22c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.1 MB (301072649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cd01113aef7e9ee6ae16d7087f3d9a349b98d1485458460a4fd258029cbc98`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126af0939b0f0fe80d45e16234ab959ce4b7569c531cbe68fecd59ad47ae146`  
		Last Modified: Tue, 04 Feb 2025 09:15:07 GMT  
		Size: 54.7 MB (54678176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76895c45ded445277d80dfcaee0f604a00263996e451eac21374f668be3a475`  
		Last Modified: Tue, 04 Feb 2025 09:15:05 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd8ed7ce48c978d4b970a58ac366fd020a171b48eb7b7c8b925cb603573ea4`  
		Last Modified: Tue, 04 Feb 2025 09:16:05 GMT  
		Size: 216.9 MB (216865531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.0-209.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:8de859316e0a14bb4af8488e3cf495f6627c554bbbab5067d2035a964224f7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadb2251094063505f367d15f604396559a03902f2d51d50f9ec86f9639ed71a`

```dockerfile
```

-	Layers:
	-	`sha256:30ea7807006b7d88217ae6800be9977d5384d0c84b8013037bebf62974c4ef2a`  
		Last Modified: Tue, 04 Feb 2025 09:15:59 GMT  
		Size: 18.0 KB (18044 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.7.0-209.1.beta-sdk`

```console
$ docker pull dart@sha256:191c03facd16f615f8b043ce5044da90bb0b59e2f95fae0ba4f9a431bd7872a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.7.0-209.1.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:05284629b12bdceb0f9846be288067855be51fce03eb67a8dda35b8b53eb143e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302428689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10d5ccbf4ad47272e6174836235fcdcf10b4f736580b8670701ad6af4f53732`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3272313418c548b6c0cc7b4923ca6948a2aa3122e80ad7dba3b3b76339475b`  
		Last Modified: Tue, 04 Feb 2025 04:39:07 GMT  
		Size: 54.9 MB (54906745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bb93547bed34a7580ede8c3bd12b8004505aa2e3220206d15ab55832c0c208`  
		Last Modified: Tue, 04 Feb 2025 04:39:07 GMT  
		Size: 1.8 MB (1796910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29c09093637bf21915ea018ba813d5d9a2577be25a9465905a0ced49557932f`  
		Last Modified: Tue, 04 Feb 2025 04:39:10 GMT  
		Size: 217.5 MB (217512699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.0-209.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:3eb8c2f317cd497c5fc437a96e8bcf7dd2c47e10230d63f09fc7ff9593285e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc342c265535be797595e62ce9cef7ee4271e2059b400b720d24e22fbd115f9`

```dockerfile
```

-	Layers:
	-	`sha256:1a716bc7926b65cdc611d3cae5764c7056064019d7d3d49cabcce3d97a8a287d`  
		Last Modified: Tue, 04 Feb 2025 04:39:06 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7.0-209.1.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:d4e0395e52c2cae1cf1fd799039b7dcaf3dad424220c2e1fdbeb5d3d791ec0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.9 MB (224928443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4264477b92316c8ff78809907e27077229e47eec70e21874b5da54d5ce748f33`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8af8a5133a30e975a3b9d74bf15cc52f8d673450261b1a58fdfcd7f3a20aeb`  
		Last Modified: Tue, 04 Feb 2025 10:50:18 GMT  
		Size: 49.6 MB (49561568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17612930c2cc3b54370d8e7a9709ce77958469f4b54a2958676f7545909b77e`  
		Last Modified: Tue, 04 Feb 2025 10:50:17 GMT  
		Size: 1.2 MB (1221681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21316a5b5b0d4084df0abf17c5b0bf5d6672435763f3c2fd27a4aeb8147a6be5`  
		Last Modified: Tue, 04 Feb 2025 10:50:21 GMT  
		Size: 150.2 MB (150230626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.0-209.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:939e154100cff3d2ab12b41cdb8d198adc770a8ed76478585802d223e124841e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c17a53a5437bcc22bb8fe18a0bee266234cec83fdad76f071a6c8150ce5e0c6`

```dockerfile
```

-	Layers:
	-	`sha256:bc72fa39423d4a92a051ffbb23a6e51a7775cf8565521c793d0656b202e8c587`  
		Last Modified: Tue, 04 Feb 2025 10:50:17 GMT  
		Size: 18.0 KB (18012 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7.0-209.1.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4fe4a41963df49f4c24e5ee381239c4a1497acd3a1bd2ba59d32f817454e22c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.1 MB (301072649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cd01113aef7e9ee6ae16d7087f3d9a349b98d1485458460a4fd258029cbc98`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126af0939b0f0fe80d45e16234ab959ce4b7569c531cbe68fecd59ad47ae146`  
		Last Modified: Tue, 04 Feb 2025 09:15:07 GMT  
		Size: 54.7 MB (54678176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76895c45ded445277d80dfcaee0f604a00263996e451eac21374f668be3a475`  
		Last Modified: Tue, 04 Feb 2025 09:15:05 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd8ed7ce48c978d4b970a58ac366fd020a171b48eb7b7c8b925cb603573ea4`  
		Last Modified: Tue, 04 Feb 2025 09:16:05 GMT  
		Size: 216.9 MB (216865531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.0-209.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8de859316e0a14bb4af8488e3cf495f6627c554bbbab5067d2035a964224f7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadb2251094063505f367d15f604396559a03902f2d51d50f9ec86f9639ed71a`

```dockerfile
```

-	Layers:
	-	`sha256:30ea7807006b7d88217ae6800be9977d5384d0c84b8013037bebf62974c4ef2a`  
		Last Modified: Tue, 04 Feb 2025 09:15:59 GMT  
		Size: 18.0 KB (18044 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:191c03facd16f615f8b043ce5044da90bb0b59e2f95fae0ba4f9a431bd7872a7
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
$ docker pull dart@sha256:05284629b12bdceb0f9846be288067855be51fce03eb67a8dda35b8b53eb143e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302428689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10d5ccbf4ad47272e6174836235fcdcf10b4f736580b8670701ad6af4f53732`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3272313418c548b6c0cc7b4923ca6948a2aa3122e80ad7dba3b3b76339475b`  
		Last Modified: Tue, 04 Feb 2025 04:39:07 GMT  
		Size: 54.9 MB (54906745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bb93547bed34a7580ede8c3bd12b8004505aa2e3220206d15ab55832c0c208`  
		Last Modified: Tue, 04 Feb 2025 04:39:07 GMT  
		Size: 1.8 MB (1796910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29c09093637bf21915ea018ba813d5d9a2577be25a9465905a0ced49557932f`  
		Last Modified: Tue, 04 Feb 2025 04:39:10 GMT  
		Size: 217.5 MB (217512699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:3eb8c2f317cd497c5fc437a96e8bcf7dd2c47e10230d63f09fc7ff9593285e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc342c265535be797595e62ce9cef7ee4271e2059b400b720d24e22fbd115f9`

```dockerfile
```

-	Layers:
	-	`sha256:1a716bc7926b65cdc611d3cae5764c7056064019d7d3d49cabcce3d97a8a287d`  
		Last Modified: Tue, 04 Feb 2025 04:39:06 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:d4e0395e52c2cae1cf1fd799039b7dcaf3dad424220c2e1fdbeb5d3d791ec0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.9 MB (224928443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4264477b92316c8ff78809907e27077229e47eec70e21874b5da54d5ce748f33`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8af8a5133a30e975a3b9d74bf15cc52f8d673450261b1a58fdfcd7f3a20aeb`  
		Last Modified: Tue, 04 Feb 2025 10:50:18 GMT  
		Size: 49.6 MB (49561568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17612930c2cc3b54370d8e7a9709ce77958469f4b54a2958676f7545909b77e`  
		Last Modified: Tue, 04 Feb 2025 10:50:17 GMT  
		Size: 1.2 MB (1221681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21316a5b5b0d4084df0abf17c5b0bf5d6672435763f3c2fd27a4aeb8147a6be5`  
		Last Modified: Tue, 04 Feb 2025 10:50:21 GMT  
		Size: 150.2 MB (150230626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:939e154100cff3d2ab12b41cdb8d198adc770a8ed76478585802d223e124841e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c17a53a5437bcc22bb8fe18a0bee266234cec83fdad76f071a6c8150ce5e0c6`

```dockerfile
```

-	Layers:
	-	`sha256:bc72fa39423d4a92a051ffbb23a6e51a7775cf8565521c793d0656b202e8c587`  
		Last Modified: Tue, 04 Feb 2025 10:50:17 GMT  
		Size: 18.0 KB (18012 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4fe4a41963df49f4c24e5ee381239c4a1497acd3a1bd2ba59d32f817454e22c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.1 MB (301072649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cd01113aef7e9ee6ae16d7087f3d9a349b98d1485458460a4fd258029cbc98`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126af0939b0f0fe80d45e16234ab959ce4b7569c531cbe68fecd59ad47ae146`  
		Last Modified: Tue, 04 Feb 2025 09:15:07 GMT  
		Size: 54.7 MB (54678176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76895c45ded445277d80dfcaee0f604a00263996e451eac21374f668be3a475`  
		Last Modified: Tue, 04 Feb 2025 09:15:05 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd8ed7ce48c978d4b970a58ac366fd020a171b48eb7b7c8b925cb603573ea4`  
		Last Modified: Tue, 04 Feb 2025 09:16:05 GMT  
		Size: 216.9 MB (216865531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:8de859316e0a14bb4af8488e3cf495f6627c554bbbab5067d2035a964224f7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadb2251094063505f367d15f604396559a03902f2d51d50f9ec86f9639ed71a`

```dockerfile
```

-	Layers:
	-	`sha256:30ea7807006b7d88217ae6800be9977d5384d0c84b8013037bebf62974c4ef2a`  
		Last Modified: Tue, 04 Feb 2025 09:15:59 GMT  
		Size: 18.0 KB (18044 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:191c03facd16f615f8b043ce5044da90bb0b59e2f95fae0ba4f9a431bd7872a7
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
$ docker pull dart@sha256:05284629b12bdceb0f9846be288067855be51fce03eb67a8dda35b8b53eb143e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302428689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10d5ccbf4ad47272e6174836235fcdcf10b4f736580b8670701ad6af4f53732`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3272313418c548b6c0cc7b4923ca6948a2aa3122e80ad7dba3b3b76339475b`  
		Last Modified: Tue, 04 Feb 2025 04:39:07 GMT  
		Size: 54.9 MB (54906745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bb93547bed34a7580ede8c3bd12b8004505aa2e3220206d15ab55832c0c208`  
		Last Modified: Tue, 04 Feb 2025 04:39:07 GMT  
		Size: 1.8 MB (1796910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29c09093637bf21915ea018ba813d5d9a2577be25a9465905a0ced49557932f`  
		Last Modified: Tue, 04 Feb 2025 04:39:10 GMT  
		Size: 217.5 MB (217512699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:3eb8c2f317cd497c5fc437a96e8bcf7dd2c47e10230d63f09fc7ff9593285e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc342c265535be797595e62ce9cef7ee4271e2059b400b720d24e22fbd115f9`

```dockerfile
```

-	Layers:
	-	`sha256:1a716bc7926b65cdc611d3cae5764c7056064019d7d3d49cabcce3d97a8a287d`  
		Last Modified: Tue, 04 Feb 2025 04:39:06 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:d4e0395e52c2cae1cf1fd799039b7dcaf3dad424220c2e1fdbeb5d3d791ec0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.9 MB (224928443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4264477b92316c8ff78809907e27077229e47eec70e21874b5da54d5ce748f33`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8af8a5133a30e975a3b9d74bf15cc52f8d673450261b1a58fdfcd7f3a20aeb`  
		Last Modified: Tue, 04 Feb 2025 10:50:18 GMT  
		Size: 49.6 MB (49561568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17612930c2cc3b54370d8e7a9709ce77958469f4b54a2958676f7545909b77e`  
		Last Modified: Tue, 04 Feb 2025 10:50:17 GMT  
		Size: 1.2 MB (1221681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21316a5b5b0d4084df0abf17c5b0bf5d6672435763f3c2fd27a4aeb8147a6be5`  
		Last Modified: Tue, 04 Feb 2025 10:50:21 GMT  
		Size: 150.2 MB (150230626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:939e154100cff3d2ab12b41cdb8d198adc770a8ed76478585802d223e124841e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c17a53a5437bcc22bb8fe18a0bee266234cec83fdad76f071a6c8150ce5e0c6`

```dockerfile
```

-	Layers:
	-	`sha256:bc72fa39423d4a92a051ffbb23a6e51a7775cf8565521c793d0656b202e8c587`  
		Last Modified: Tue, 04 Feb 2025 10:50:17 GMT  
		Size: 18.0 KB (18012 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4fe4a41963df49f4c24e5ee381239c4a1497acd3a1bd2ba59d32f817454e22c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.1 MB (301072649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cd01113aef7e9ee6ae16d7087f3d9a349b98d1485458460a4fd258029cbc98`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126af0939b0f0fe80d45e16234ab959ce4b7569c531cbe68fecd59ad47ae146`  
		Last Modified: Tue, 04 Feb 2025 09:15:07 GMT  
		Size: 54.7 MB (54678176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76895c45ded445277d80dfcaee0f604a00263996e451eac21374f668be3a475`  
		Last Modified: Tue, 04 Feb 2025 09:15:05 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd8ed7ce48c978d4b970a58ac366fd020a171b48eb7b7c8b925cb603573ea4`  
		Last Modified: Tue, 04 Feb 2025 09:16:05 GMT  
		Size: 216.9 MB (216865531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8de859316e0a14bb4af8488e3cf495f6627c554bbbab5067d2035a964224f7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadb2251094063505f367d15f604396559a03902f2d51d50f9ec86f9639ed71a`

```dockerfile
```

-	Layers:
	-	`sha256:30ea7807006b7d88217ae6800be9977d5384d0c84b8013037bebf62974c4ef2a`  
		Last Modified: Tue, 04 Feb 2025 09:15:59 GMT  
		Size: 18.0 KB (18044 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:032365a0d5255fe25674d49ab62cca5967e7f68d6d9c9bec6fd5f431daec9c30
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
$ docker pull dart@sha256:54ff82f6115ca4dd37d996ec8e4a147f1bfad3d13c6727d41fa72dbd6be93014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312109862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f12c4e4e00c168ba5b03d030436bf02b42196e3c59431563b45a2b4ac26d69`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc7cd33f899e4916e106343a4113582014e4f881bf6450fcfd9895b97144128`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 54.9 MB (54906759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76dc3d94143d68fa2c1275b3b5818e40ff1e814c8dbd437bab043c0a86d53a5`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 1.8 MB (1796901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558a6aaaa919082dfa0c6a496de4b31e2b411ac34c5dc44c6daa7daa5f1a1e12`  
		Last Modified: Tue, 04 Feb 2025 04:39:01 GMT  
		Size: 227.2 MB (227193867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:b52d4615255da33008bad8c9435f8b75cd6a77cd7a2b16354b2607fd8326bc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9880eca97e150d3af6afd4138bdecf47c64f17251078d7ee2f3e9605d405f4`

```dockerfile
```

-	Layers:
	-	`sha256:cf60c365df752c55eeebfca95b9ed8bf6f897ab517f78568cb645091d664e6b4`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:da2f3a7a5c08d691552eb23f673dfc18a4b04be147427d571f29acfc6a4e5729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210395961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f297840472ff7b5b8a16c48469f8a8a5d157ef34ff1832b4cd13e73bfb1d06`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1b2dab5a73d378cc31835ab53f09fb017cb86b517a3b983911442a2d031149`  
		Last Modified: Tue, 04 Feb 2025 10:49:05 GMT  
		Size: 49.6 MB (49561346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef7554d5be4301c1388ee54c011ee6ea7e854972805f5d3e2ab4c2aa4c995d`  
		Last Modified: Tue, 04 Feb 2025 10:49:03 GMT  
		Size: 1.2 MB (1221672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756485da8bc62b90f72a0888b60302d5dd366a23d1991fa57fa36696efe1eba7`  
		Last Modified: Tue, 04 Feb 2025 10:49:07 GMT  
		Size: 135.7 MB (135698375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:4cf6c57feb50a6a416e26b63c0c1f359b00641479c3314eed783d9300d14c7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7b07ad7d4ff87adacda784c76a6cecf85b72fa57f5e03be879be6d4f009294`

```dockerfile
```

-	Layers:
	-	`sha256:1922626f788f7f2f113503744e0ce772858422592a4af70e482e87c4b0fd19e7`  
		Last Modified: Tue, 04 Feb 2025 10:49:03 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:a0c55f1753b9ff278bd0ee678df370d694ea10368b1d7f6d541db2f0ac204e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310566943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27acde1cc697fa5419a877250603d4105d19c22e42fe8ef1800e07408a91b42`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126af0939b0f0fe80d45e16234ab959ce4b7569c531cbe68fecd59ad47ae146`  
		Last Modified: Tue, 04 Feb 2025 09:15:07 GMT  
		Size: 54.7 MB (54678176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76895c45ded445277d80dfcaee0f604a00263996e451eac21374f668be3a475`  
		Last Modified: Tue, 04 Feb 2025 09:15:05 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad043eee0fb851a491b72173522e3bbc03336c27dad17069a3e22e2820dc2f4`  
		Last Modified: Tue, 04 Feb 2025 09:15:10 GMT  
		Size: 226.4 MB (226359825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:11984afe369c09c981cee162fbcce42137610edc1ebce78d802cd27e98e90f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ed972963d0876d62e4a5ead5a164642912ce5004180aa897645637dea888f6`

```dockerfile
```

-	Layers:
	-	`sha256:a18cf7749b6b46e33600329e8fceaf8dce378e5975fe8195e32a7d3562738cf0`  
		Last Modified: Tue, 04 Feb 2025 09:15:05 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:032365a0d5255fe25674d49ab62cca5967e7f68d6d9c9bec6fd5f431daec9c30
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
$ docker pull dart@sha256:54ff82f6115ca4dd37d996ec8e4a147f1bfad3d13c6727d41fa72dbd6be93014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312109862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f12c4e4e00c168ba5b03d030436bf02b42196e3c59431563b45a2b4ac26d69`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc7cd33f899e4916e106343a4113582014e4f881bf6450fcfd9895b97144128`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 54.9 MB (54906759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76dc3d94143d68fa2c1275b3b5818e40ff1e814c8dbd437bab043c0a86d53a5`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 1.8 MB (1796901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558a6aaaa919082dfa0c6a496de4b31e2b411ac34c5dc44c6daa7daa5f1a1e12`  
		Last Modified: Tue, 04 Feb 2025 04:39:01 GMT  
		Size: 227.2 MB (227193867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b52d4615255da33008bad8c9435f8b75cd6a77cd7a2b16354b2607fd8326bc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9880eca97e150d3af6afd4138bdecf47c64f17251078d7ee2f3e9605d405f4`

```dockerfile
```

-	Layers:
	-	`sha256:cf60c365df752c55eeebfca95b9ed8bf6f897ab517f78568cb645091d664e6b4`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:da2f3a7a5c08d691552eb23f673dfc18a4b04be147427d571f29acfc6a4e5729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210395961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f297840472ff7b5b8a16c48469f8a8a5d157ef34ff1832b4cd13e73bfb1d06`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1b2dab5a73d378cc31835ab53f09fb017cb86b517a3b983911442a2d031149`  
		Last Modified: Tue, 04 Feb 2025 10:49:05 GMT  
		Size: 49.6 MB (49561346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef7554d5be4301c1388ee54c011ee6ea7e854972805f5d3e2ab4c2aa4c995d`  
		Last Modified: Tue, 04 Feb 2025 10:49:03 GMT  
		Size: 1.2 MB (1221672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756485da8bc62b90f72a0888b60302d5dd366a23d1991fa57fa36696efe1eba7`  
		Last Modified: Tue, 04 Feb 2025 10:49:07 GMT  
		Size: 135.7 MB (135698375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4cf6c57feb50a6a416e26b63c0c1f359b00641479c3314eed783d9300d14c7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7b07ad7d4ff87adacda784c76a6cecf85b72fa57f5e03be879be6d4f009294`

```dockerfile
```

-	Layers:
	-	`sha256:1922626f788f7f2f113503744e0ce772858422592a4af70e482e87c4b0fd19e7`  
		Last Modified: Tue, 04 Feb 2025 10:49:03 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:a0c55f1753b9ff278bd0ee678df370d694ea10368b1d7f6d541db2f0ac204e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310566943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27acde1cc697fa5419a877250603d4105d19c22e42fe8ef1800e07408a91b42`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126af0939b0f0fe80d45e16234ab959ce4b7569c531cbe68fecd59ad47ae146`  
		Last Modified: Tue, 04 Feb 2025 09:15:07 GMT  
		Size: 54.7 MB (54678176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76895c45ded445277d80dfcaee0f604a00263996e451eac21374f668be3a475`  
		Last Modified: Tue, 04 Feb 2025 09:15:05 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad043eee0fb851a491b72173522e3bbc03336c27dad17069a3e22e2820dc2f4`  
		Last Modified: Tue, 04 Feb 2025 09:15:10 GMT  
		Size: 226.4 MB (226359825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:11984afe369c09c981cee162fbcce42137610edc1ebce78d802cd27e98e90f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ed972963d0876d62e4a5ead5a164642912ce5004180aa897645637dea888f6`

```dockerfile
```

-	Layers:
	-	`sha256:a18cf7749b6b46e33600329e8fceaf8dce378e5975fe8195e32a7d3562738cf0`  
		Last Modified: Tue, 04 Feb 2025 09:15:05 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:032365a0d5255fe25674d49ab62cca5967e7f68d6d9c9bec6fd5f431daec9c30
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
$ docker pull dart@sha256:54ff82f6115ca4dd37d996ec8e4a147f1bfad3d13c6727d41fa72dbd6be93014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312109862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f12c4e4e00c168ba5b03d030436bf02b42196e3c59431563b45a2b4ac26d69`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc7cd33f899e4916e106343a4113582014e4f881bf6450fcfd9895b97144128`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 54.9 MB (54906759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76dc3d94143d68fa2c1275b3b5818e40ff1e814c8dbd437bab043c0a86d53a5`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 1.8 MB (1796901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558a6aaaa919082dfa0c6a496de4b31e2b411ac34c5dc44c6daa7daa5f1a1e12`  
		Last Modified: Tue, 04 Feb 2025 04:39:01 GMT  
		Size: 227.2 MB (227193867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:b52d4615255da33008bad8c9435f8b75cd6a77cd7a2b16354b2607fd8326bc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9880eca97e150d3af6afd4138bdecf47c64f17251078d7ee2f3e9605d405f4`

```dockerfile
```

-	Layers:
	-	`sha256:cf60c365df752c55eeebfca95b9ed8bf6f897ab517f78568cb645091d664e6b4`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:da2f3a7a5c08d691552eb23f673dfc18a4b04be147427d571f29acfc6a4e5729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210395961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f297840472ff7b5b8a16c48469f8a8a5d157ef34ff1832b4cd13e73bfb1d06`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1b2dab5a73d378cc31835ab53f09fb017cb86b517a3b983911442a2d031149`  
		Last Modified: Tue, 04 Feb 2025 10:49:05 GMT  
		Size: 49.6 MB (49561346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef7554d5be4301c1388ee54c011ee6ea7e854972805f5d3e2ab4c2aa4c995d`  
		Last Modified: Tue, 04 Feb 2025 10:49:03 GMT  
		Size: 1.2 MB (1221672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756485da8bc62b90f72a0888b60302d5dd366a23d1991fa57fa36696efe1eba7`  
		Last Modified: Tue, 04 Feb 2025 10:49:07 GMT  
		Size: 135.7 MB (135698375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:4cf6c57feb50a6a416e26b63c0c1f359b00641479c3314eed783d9300d14c7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7b07ad7d4ff87adacda784c76a6cecf85b72fa57f5e03be879be6d4f009294`

```dockerfile
```

-	Layers:
	-	`sha256:1922626f788f7f2f113503744e0ce772858422592a4af70e482e87c4b0fd19e7`  
		Last Modified: Tue, 04 Feb 2025 10:49:03 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:a0c55f1753b9ff278bd0ee678df370d694ea10368b1d7f6d541db2f0ac204e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310566943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27acde1cc697fa5419a877250603d4105d19c22e42fe8ef1800e07408a91b42`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126af0939b0f0fe80d45e16234ab959ce4b7569c531cbe68fecd59ad47ae146`  
		Last Modified: Tue, 04 Feb 2025 09:15:07 GMT  
		Size: 54.7 MB (54678176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76895c45ded445277d80dfcaee0f604a00263996e451eac21374f668be3a475`  
		Last Modified: Tue, 04 Feb 2025 09:15:05 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad043eee0fb851a491b72173522e3bbc03336c27dad17069a3e22e2820dc2f4`  
		Last Modified: Tue, 04 Feb 2025 09:15:10 GMT  
		Size: 226.4 MB (226359825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:11984afe369c09c981cee162fbcce42137610edc1ebce78d802cd27e98e90f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ed972963d0876d62e4a5ead5a164642912ce5004180aa897645637dea888f6`

```dockerfile
```

-	Layers:
	-	`sha256:a18cf7749b6b46e33600329e8fceaf8dce378e5975fe8195e32a7d3562738cf0`  
		Last Modified: Tue, 04 Feb 2025 09:15:05 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:032365a0d5255fe25674d49ab62cca5967e7f68d6d9c9bec6fd5f431daec9c30
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
$ docker pull dart@sha256:54ff82f6115ca4dd37d996ec8e4a147f1bfad3d13c6727d41fa72dbd6be93014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312109862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f12c4e4e00c168ba5b03d030436bf02b42196e3c59431563b45a2b4ac26d69`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc7cd33f899e4916e106343a4113582014e4f881bf6450fcfd9895b97144128`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 54.9 MB (54906759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76dc3d94143d68fa2c1275b3b5818e40ff1e814c8dbd437bab043c0a86d53a5`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 1.8 MB (1796901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558a6aaaa919082dfa0c6a496de4b31e2b411ac34c5dc44c6daa7daa5f1a1e12`  
		Last Modified: Tue, 04 Feb 2025 04:39:01 GMT  
		Size: 227.2 MB (227193867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b52d4615255da33008bad8c9435f8b75cd6a77cd7a2b16354b2607fd8326bc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9880eca97e150d3af6afd4138bdecf47c64f17251078d7ee2f3e9605d405f4`

```dockerfile
```

-	Layers:
	-	`sha256:cf60c365df752c55eeebfca95b9ed8bf6f897ab517f78568cb645091d664e6b4`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:da2f3a7a5c08d691552eb23f673dfc18a4b04be147427d571f29acfc6a4e5729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210395961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f297840472ff7b5b8a16c48469f8a8a5d157ef34ff1832b4cd13e73bfb1d06`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1b2dab5a73d378cc31835ab53f09fb017cb86b517a3b983911442a2d031149`  
		Last Modified: Tue, 04 Feb 2025 10:49:05 GMT  
		Size: 49.6 MB (49561346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef7554d5be4301c1388ee54c011ee6ea7e854972805f5d3e2ab4c2aa4c995d`  
		Last Modified: Tue, 04 Feb 2025 10:49:03 GMT  
		Size: 1.2 MB (1221672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756485da8bc62b90f72a0888b60302d5dd366a23d1991fa57fa36696efe1eba7`  
		Last Modified: Tue, 04 Feb 2025 10:49:07 GMT  
		Size: 135.7 MB (135698375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4cf6c57feb50a6a416e26b63c0c1f359b00641479c3314eed783d9300d14c7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7b07ad7d4ff87adacda784c76a6cecf85b72fa57f5e03be879be6d4f009294`

```dockerfile
```

-	Layers:
	-	`sha256:1922626f788f7f2f113503744e0ce772858422592a4af70e482e87c4b0fd19e7`  
		Last Modified: Tue, 04 Feb 2025 10:49:03 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:a0c55f1753b9ff278bd0ee678df370d694ea10368b1d7f6d541db2f0ac204e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310566943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27acde1cc697fa5419a877250603d4105d19c22e42fe8ef1800e07408a91b42`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126af0939b0f0fe80d45e16234ab959ce4b7569c531cbe68fecd59ad47ae146`  
		Last Modified: Tue, 04 Feb 2025 09:15:07 GMT  
		Size: 54.7 MB (54678176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76895c45ded445277d80dfcaee0f604a00263996e451eac21374f668be3a475`  
		Last Modified: Tue, 04 Feb 2025 09:15:05 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad043eee0fb851a491b72173522e3bbc03336c27dad17069a3e22e2820dc2f4`  
		Last Modified: Tue, 04 Feb 2025 09:15:10 GMT  
		Size: 226.4 MB (226359825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:11984afe369c09c981cee162fbcce42137610edc1ebce78d802cd27e98e90f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ed972963d0876d62e4a5ead5a164642912ce5004180aa897645637dea888f6`

```dockerfile
```

-	Layers:
	-	`sha256:a18cf7749b6b46e33600329e8fceaf8dce378e5975fe8195e32a7d3562738cf0`  
		Last Modified: Tue, 04 Feb 2025 09:15:05 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json
