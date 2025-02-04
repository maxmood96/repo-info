<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.6`](#dart36)
-	[`dart:3.6-sdk`](#dart36-sdk)
-	[`dart:3.6.2`](#dart362)
-	[`dart:3.6.2-sdk`](#dart362-sdk)
-	[`dart:3.7.0-323.2.beta`](#dart370-3232beta)
-	[`dart:3.7.0-323.2.beta-sdk`](#dart370-3232beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:d30a0e827230c3419f90022fb821ba69c96d3b1ab98b0914aa983f3950617399
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
$ docker pull dart@sha256:553d8f8fc187ab31ad8f8ed9c4722c812057607e10a7dc5d4bb7d7e89def2c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312140840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3495d6c4d34ccf3d7457b9ecdfc1cc526891f9f4f09e260924d7e9915832923`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0785300a74e92d61d24e3d60a87edaff62d5ede8e74f2e8368f0c52408c49cee`  
		Last Modified: Tue, 04 Feb 2025 19:33:06 GMT  
		Size: 54.9 MB (54906742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9859598bb5e58e0449dd2866c56d84cc61eb6220a6b0508aa6717600b468fda`  
		Last Modified: Tue, 04 Feb 2025 19:33:05 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca07202c9e54f4fe2ceb63a5856929c2c74bd045a48581925abbaa393f8bba`  
		Last Modified: Tue, 04 Feb 2025 19:33:10 GMT  
		Size: 227.2 MB (227224845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:1ce94f4cc12a1678ea21e42b3970f8b3f1723599e5fd7ef168d772be9205601c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed10b94ea5d6396292c54f541f7004b4390ccf05184e6229a761784f235ff72`

```dockerfile
```

-	Layers:
	-	`sha256:e56081c707bee6a58dc1960a59c9511d6fb5dfce8beb6b34713ee777d1b2169e`  
		Last Modified: Tue, 04 Feb 2025 19:33:04 GMT  
		Size: 19.6 KB (19600 bytes)  
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
$ docker pull dart@sha256:d30a0e827230c3419f90022fb821ba69c96d3b1ab98b0914aa983f3950617399
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
$ docker pull dart@sha256:553d8f8fc187ab31ad8f8ed9c4722c812057607e10a7dc5d4bb7d7e89def2c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312140840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3495d6c4d34ccf3d7457b9ecdfc1cc526891f9f4f09e260924d7e9915832923`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0785300a74e92d61d24e3d60a87edaff62d5ede8e74f2e8368f0c52408c49cee`  
		Last Modified: Tue, 04 Feb 2025 19:33:06 GMT  
		Size: 54.9 MB (54906742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9859598bb5e58e0449dd2866c56d84cc61eb6220a6b0508aa6717600b468fda`  
		Last Modified: Tue, 04 Feb 2025 19:33:05 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca07202c9e54f4fe2ceb63a5856929c2c74bd045a48581925abbaa393f8bba`  
		Last Modified: Tue, 04 Feb 2025 19:33:10 GMT  
		Size: 227.2 MB (227224845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1ce94f4cc12a1678ea21e42b3970f8b3f1723599e5fd7ef168d772be9205601c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed10b94ea5d6396292c54f541f7004b4390ccf05184e6229a761784f235ff72`

```dockerfile
```

-	Layers:
	-	`sha256:e56081c707bee6a58dc1960a59c9511d6fb5dfce8beb6b34713ee777d1b2169e`  
		Last Modified: Tue, 04 Feb 2025 19:33:04 GMT  
		Size: 19.6 KB (19600 bytes)  
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
$ docker pull dart@sha256:d30a0e827230c3419f90022fb821ba69c96d3b1ab98b0914aa983f3950617399
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
$ docker pull dart@sha256:553d8f8fc187ab31ad8f8ed9c4722c812057607e10a7dc5d4bb7d7e89def2c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312140840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3495d6c4d34ccf3d7457b9ecdfc1cc526891f9f4f09e260924d7e9915832923`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0785300a74e92d61d24e3d60a87edaff62d5ede8e74f2e8368f0c52408c49cee`  
		Last Modified: Tue, 04 Feb 2025 19:33:06 GMT  
		Size: 54.9 MB (54906742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9859598bb5e58e0449dd2866c56d84cc61eb6220a6b0508aa6717600b468fda`  
		Last Modified: Tue, 04 Feb 2025 19:33:05 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca07202c9e54f4fe2ceb63a5856929c2c74bd045a48581925abbaa393f8bba`  
		Last Modified: Tue, 04 Feb 2025 19:33:10 GMT  
		Size: 227.2 MB (227224845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6` - unknown; unknown

```console
$ docker pull dart@sha256:1ce94f4cc12a1678ea21e42b3970f8b3f1723599e5fd7ef168d772be9205601c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed10b94ea5d6396292c54f541f7004b4390ccf05184e6229a761784f235ff72`

```dockerfile
```

-	Layers:
	-	`sha256:e56081c707bee6a58dc1960a59c9511d6fb5dfce8beb6b34713ee777d1b2169e`  
		Last Modified: Tue, 04 Feb 2025 19:33:04 GMT  
		Size: 19.6 KB (19600 bytes)  
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
$ docker pull dart@sha256:d30a0e827230c3419f90022fb821ba69c96d3b1ab98b0914aa983f3950617399
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
$ docker pull dart@sha256:553d8f8fc187ab31ad8f8ed9c4722c812057607e10a7dc5d4bb7d7e89def2c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312140840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3495d6c4d34ccf3d7457b9ecdfc1cc526891f9f4f09e260924d7e9915832923`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0785300a74e92d61d24e3d60a87edaff62d5ede8e74f2e8368f0c52408c49cee`  
		Last Modified: Tue, 04 Feb 2025 19:33:06 GMT  
		Size: 54.9 MB (54906742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9859598bb5e58e0449dd2866c56d84cc61eb6220a6b0508aa6717600b468fda`  
		Last Modified: Tue, 04 Feb 2025 19:33:05 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca07202c9e54f4fe2ceb63a5856929c2c74bd045a48581925abbaa393f8bba`  
		Last Modified: Tue, 04 Feb 2025 19:33:10 GMT  
		Size: 227.2 MB (227224845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1ce94f4cc12a1678ea21e42b3970f8b3f1723599e5fd7ef168d772be9205601c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed10b94ea5d6396292c54f541f7004b4390ccf05184e6229a761784f235ff72`

```dockerfile
```

-	Layers:
	-	`sha256:e56081c707bee6a58dc1960a59c9511d6fb5dfce8beb6b34713ee777d1b2169e`  
		Last Modified: Tue, 04 Feb 2025 19:33:04 GMT  
		Size: 19.6 KB (19600 bytes)  
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

## `dart:3.6.2`

```console
$ docker pull dart@sha256:37de11c295c32a99a2b70b912f908c5bd2cae2096dcb588cf818b368de1cff49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `dart:3.6.2` - linux; amd64

```console
$ docker pull dart@sha256:553d8f8fc187ab31ad8f8ed9c4722c812057607e10a7dc5d4bb7d7e89def2c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312140840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3495d6c4d34ccf3d7457b9ecdfc1cc526891f9f4f09e260924d7e9915832923`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0785300a74e92d61d24e3d60a87edaff62d5ede8e74f2e8368f0c52408c49cee`  
		Last Modified: Tue, 04 Feb 2025 19:33:06 GMT  
		Size: 54.9 MB (54906742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9859598bb5e58e0449dd2866c56d84cc61eb6220a6b0508aa6717600b468fda`  
		Last Modified: Tue, 04 Feb 2025 19:33:05 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca07202c9e54f4fe2ceb63a5856929c2c74bd045a48581925abbaa393f8bba`  
		Last Modified: Tue, 04 Feb 2025 19:33:10 GMT  
		Size: 227.2 MB (227224845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6.2` - unknown; unknown

```console
$ docker pull dart@sha256:1ce94f4cc12a1678ea21e42b3970f8b3f1723599e5fd7ef168d772be9205601c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed10b94ea5d6396292c54f541f7004b4390ccf05184e6229a761784f235ff72`

```dockerfile
```

-	Layers:
	-	`sha256:e56081c707bee6a58dc1960a59c9511d6fb5dfce8beb6b34713ee777d1b2169e`  
		Last Modified: Tue, 04 Feb 2025 19:33:04 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.6.2-sdk`

```console
$ docker pull dart@sha256:37de11c295c32a99a2b70b912f908c5bd2cae2096dcb588cf818b368de1cff49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `dart:3.6.2-sdk` - linux; amd64

```console
$ docker pull dart@sha256:553d8f8fc187ab31ad8f8ed9c4722c812057607e10a7dc5d4bb7d7e89def2c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312140840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3495d6c4d34ccf3d7457b9ecdfc1cc526891f9f4f09e260924d7e9915832923`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0785300a74e92d61d24e3d60a87edaff62d5ede8e74f2e8368f0c52408c49cee`  
		Last Modified: Tue, 04 Feb 2025 19:33:06 GMT  
		Size: 54.9 MB (54906742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9859598bb5e58e0449dd2866c56d84cc61eb6220a6b0508aa6717600b468fda`  
		Last Modified: Tue, 04 Feb 2025 19:33:05 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca07202c9e54f4fe2ceb63a5856929c2c74bd045a48581925abbaa393f8bba`  
		Last Modified: Tue, 04 Feb 2025 19:33:10 GMT  
		Size: 227.2 MB (227224845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6.2-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1ce94f4cc12a1678ea21e42b3970f8b3f1723599e5fd7ef168d772be9205601c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed10b94ea5d6396292c54f541f7004b4390ccf05184e6229a761784f235ff72`

```dockerfile
```

-	Layers:
	-	`sha256:e56081c707bee6a58dc1960a59c9511d6fb5dfce8beb6b34713ee777d1b2169e`  
		Last Modified: Tue, 04 Feb 2025 19:33:04 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.7.0-323.2.beta`

```console
$ docker pull dart@sha256:d492e5d7848689a810585e246c03f49c1d60ec6610ae3e7c2ffa28c379e5600b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `dart:3.7.0-323.2.beta` - linux; amd64

```console
$ docker pull dart@sha256:659c1501cf02b0f21a4ffd53b8997fe25d2d4a956e64e7c07988bcccef9d08ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304792577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5878d61e671d976f90eb43c4e9a93b5d072c7f4810d3323cbcaef61aeaf0ccd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=77a239e591f2191ce0f1a7303ef536de4103ed4dd45201b08c77a67ee9cb09f5;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ccdf0b9c0b7cd59c4993fdda32ec36e90c56deacc43bd58087ced4b23f198d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f6b865b4447eeb71b5f6b179e1c38bba0f758b808baae48eac80f9348801b67e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-323.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5385fb88aa23fb935cf7e52dca4b4f05b1bdd1eccf5aa0cf4a18be210105f2`  
		Last Modified: Tue, 04 Feb 2025 19:32:58 GMT  
		Size: 54.9 MB (54906681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30514d202daad92a9467c3613526b164fa603c35330feda04b1d625137994ad9`  
		Last Modified: Tue, 04 Feb 2025 19:32:57 GMT  
		Size: 1.8 MB (1796916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1b654771c20f95f5342cbd0387d3c08d9b342d274ceeffd676bb93607d0e94`  
		Last Modified: Tue, 04 Feb 2025 19:33:00 GMT  
		Size: 219.9 MB (219876645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.0-323.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:435f8a7d58943d058226f46d70ca967d02cfe74136a7ee6bde6aceadeb53fa2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02dcccbf7cf1f27a33a31431ccd5258649bd69b58f8c869331ef3189c3afa790`

```dockerfile
```

-	Layers:
	-	`sha256:84c8a26fccabb9e8e022a29c10134da751cb90b2ae3a6f5551f0fc0eb54626b4`  
		Last Modified: Tue, 04 Feb 2025 19:32:57 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.7.0-323.2.beta-sdk`

```console
$ docker pull dart@sha256:d492e5d7848689a810585e246c03f49c1d60ec6610ae3e7c2ffa28c379e5600b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `dart:3.7.0-323.2.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:659c1501cf02b0f21a4ffd53b8997fe25d2d4a956e64e7c07988bcccef9d08ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304792577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5878d61e671d976f90eb43c4e9a93b5d072c7f4810d3323cbcaef61aeaf0ccd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=77a239e591f2191ce0f1a7303ef536de4103ed4dd45201b08c77a67ee9cb09f5;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ccdf0b9c0b7cd59c4993fdda32ec36e90c56deacc43bd58087ced4b23f198d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f6b865b4447eeb71b5f6b179e1c38bba0f758b808baae48eac80f9348801b67e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-323.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5385fb88aa23fb935cf7e52dca4b4f05b1bdd1eccf5aa0cf4a18be210105f2`  
		Last Modified: Tue, 04 Feb 2025 19:32:58 GMT  
		Size: 54.9 MB (54906681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30514d202daad92a9467c3613526b164fa603c35330feda04b1d625137994ad9`  
		Last Modified: Tue, 04 Feb 2025 19:32:57 GMT  
		Size: 1.8 MB (1796916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1b654771c20f95f5342cbd0387d3c08d9b342d274ceeffd676bb93607d0e94`  
		Last Modified: Tue, 04 Feb 2025 19:33:00 GMT  
		Size: 219.9 MB (219876645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.0-323.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:435f8a7d58943d058226f46d70ca967d02cfe74136a7ee6bde6aceadeb53fa2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02dcccbf7cf1f27a33a31431ccd5258649bd69b58f8c869331ef3189c3afa790`

```dockerfile
```

-	Layers:
	-	`sha256:84c8a26fccabb9e8e022a29c10134da751cb90b2ae3a6f5551f0fc0eb54626b4`  
		Last Modified: Tue, 04 Feb 2025 19:32:57 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:904e90c838fe0f70c478adcb8abb520380bf9be9f747ece30af6f7f5fb57c340
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
$ docker pull dart@sha256:659c1501cf02b0f21a4ffd53b8997fe25d2d4a956e64e7c07988bcccef9d08ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304792577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5878d61e671d976f90eb43c4e9a93b5d072c7f4810d3323cbcaef61aeaf0ccd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=77a239e591f2191ce0f1a7303ef536de4103ed4dd45201b08c77a67ee9cb09f5;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ccdf0b9c0b7cd59c4993fdda32ec36e90c56deacc43bd58087ced4b23f198d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f6b865b4447eeb71b5f6b179e1c38bba0f758b808baae48eac80f9348801b67e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-323.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5385fb88aa23fb935cf7e52dca4b4f05b1bdd1eccf5aa0cf4a18be210105f2`  
		Last Modified: Tue, 04 Feb 2025 19:32:58 GMT  
		Size: 54.9 MB (54906681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30514d202daad92a9467c3613526b164fa603c35330feda04b1d625137994ad9`  
		Last Modified: Tue, 04 Feb 2025 19:32:57 GMT  
		Size: 1.8 MB (1796916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1b654771c20f95f5342cbd0387d3c08d9b342d274ceeffd676bb93607d0e94`  
		Last Modified: Tue, 04 Feb 2025 19:33:00 GMT  
		Size: 219.9 MB (219876645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:435f8a7d58943d058226f46d70ca967d02cfe74136a7ee6bde6aceadeb53fa2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02dcccbf7cf1f27a33a31431ccd5258649bd69b58f8c869331ef3189c3afa790`

```dockerfile
```

-	Layers:
	-	`sha256:84c8a26fccabb9e8e022a29c10134da751cb90b2ae3a6f5551f0fc0eb54626b4`  
		Last Modified: Tue, 04 Feb 2025 19:32:57 GMT  
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
$ docker pull dart@sha256:904e90c838fe0f70c478adcb8abb520380bf9be9f747ece30af6f7f5fb57c340
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
$ docker pull dart@sha256:659c1501cf02b0f21a4ffd53b8997fe25d2d4a956e64e7c07988bcccef9d08ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304792577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5878d61e671d976f90eb43c4e9a93b5d072c7f4810d3323cbcaef61aeaf0ccd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=77a239e591f2191ce0f1a7303ef536de4103ed4dd45201b08c77a67ee9cb09f5;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ccdf0b9c0b7cd59c4993fdda32ec36e90c56deacc43bd58087ced4b23f198d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f6b865b4447eeb71b5f6b179e1c38bba0f758b808baae48eac80f9348801b67e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-323.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5385fb88aa23fb935cf7e52dca4b4f05b1bdd1eccf5aa0cf4a18be210105f2`  
		Last Modified: Tue, 04 Feb 2025 19:32:58 GMT  
		Size: 54.9 MB (54906681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30514d202daad92a9467c3613526b164fa603c35330feda04b1d625137994ad9`  
		Last Modified: Tue, 04 Feb 2025 19:32:57 GMT  
		Size: 1.8 MB (1796916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1b654771c20f95f5342cbd0387d3c08d9b342d274ceeffd676bb93607d0e94`  
		Last Modified: Tue, 04 Feb 2025 19:33:00 GMT  
		Size: 219.9 MB (219876645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:435f8a7d58943d058226f46d70ca967d02cfe74136a7ee6bde6aceadeb53fa2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02dcccbf7cf1f27a33a31431ccd5258649bd69b58f8c869331ef3189c3afa790`

```dockerfile
```

-	Layers:
	-	`sha256:84c8a26fccabb9e8e022a29c10134da751cb90b2ae3a6f5551f0fc0eb54626b4`  
		Last Modified: Tue, 04 Feb 2025 19:32:57 GMT  
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
$ docker pull dart@sha256:d30a0e827230c3419f90022fb821ba69c96d3b1ab98b0914aa983f3950617399
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
$ docker pull dart@sha256:553d8f8fc187ab31ad8f8ed9c4722c812057607e10a7dc5d4bb7d7e89def2c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312140840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3495d6c4d34ccf3d7457b9ecdfc1cc526891f9f4f09e260924d7e9915832923`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0785300a74e92d61d24e3d60a87edaff62d5ede8e74f2e8368f0c52408c49cee`  
		Last Modified: Tue, 04 Feb 2025 19:33:06 GMT  
		Size: 54.9 MB (54906742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9859598bb5e58e0449dd2866c56d84cc61eb6220a6b0508aa6717600b468fda`  
		Last Modified: Tue, 04 Feb 2025 19:33:05 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca07202c9e54f4fe2ceb63a5856929c2c74bd045a48581925abbaa393f8bba`  
		Last Modified: Tue, 04 Feb 2025 19:33:10 GMT  
		Size: 227.2 MB (227224845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:1ce94f4cc12a1678ea21e42b3970f8b3f1723599e5fd7ef168d772be9205601c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed10b94ea5d6396292c54f541f7004b4390ccf05184e6229a761784f235ff72`

```dockerfile
```

-	Layers:
	-	`sha256:e56081c707bee6a58dc1960a59c9511d6fb5dfce8beb6b34713ee777d1b2169e`  
		Last Modified: Tue, 04 Feb 2025 19:33:04 GMT  
		Size: 19.6 KB (19600 bytes)  
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
$ docker pull dart@sha256:d30a0e827230c3419f90022fb821ba69c96d3b1ab98b0914aa983f3950617399
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
$ docker pull dart@sha256:553d8f8fc187ab31ad8f8ed9c4722c812057607e10a7dc5d4bb7d7e89def2c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312140840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3495d6c4d34ccf3d7457b9ecdfc1cc526891f9f4f09e260924d7e9915832923`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0785300a74e92d61d24e3d60a87edaff62d5ede8e74f2e8368f0c52408c49cee`  
		Last Modified: Tue, 04 Feb 2025 19:33:06 GMT  
		Size: 54.9 MB (54906742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9859598bb5e58e0449dd2866c56d84cc61eb6220a6b0508aa6717600b468fda`  
		Last Modified: Tue, 04 Feb 2025 19:33:05 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca07202c9e54f4fe2ceb63a5856929c2c74bd045a48581925abbaa393f8bba`  
		Last Modified: Tue, 04 Feb 2025 19:33:10 GMT  
		Size: 227.2 MB (227224845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1ce94f4cc12a1678ea21e42b3970f8b3f1723599e5fd7ef168d772be9205601c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed10b94ea5d6396292c54f541f7004b4390ccf05184e6229a761784f235ff72`

```dockerfile
```

-	Layers:
	-	`sha256:e56081c707bee6a58dc1960a59c9511d6fb5dfce8beb6b34713ee777d1b2169e`  
		Last Modified: Tue, 04 Feb 2025 19:33:04 GMT  
		Size: 19.6 KB (19600 bytes)  
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
$ docker pull dart@sha256:d30a0e827230c3419f90022fb821ba69c96d3b1ab98b0914aa983f3950617399
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
$ docker pull dart@sha256:553d8f8fc187ab31ad8f8ed9c4722c812057607e10a7dc5d4bb7d7e89def2c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312140840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3495d6c4d34ccf3d7457b9ecdfc1cc526891f9f4f09e260924d7e9915832923`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0785300a74e92d61d24e3d60a87edaff62d5ede8e74f2e8368f0c52408c49cee`  
		Last Modified: Tue, 04 Feb 2025 19:33:06 GMT  
		Size: 54.9 MB (54906742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9859598bb5e58e0449dd2866c56d84cc61eb6220a6b0508aa6717600b468fda`  
		Last Modified: Tue, 04 Feb 2025 19:33:05 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca07202c9e54f4fe2ceb63a5856929c2c74bd045a48581925abbaa393f8bba`  
		Last Modified: Tue, 04 Feb 2025 19:33:10 GMT  
		Size: 227.2 MB (227224845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:1ce94f4cc12a1678ea21e42b3970f8b3f1723599e5fd7ef168d772be9205601c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed10b94ea5d6396292c54f541f7004b4390ccf05184e6229a761784f235ff72`

```dockerfile
```

-	Layers:
	-	`sha256:e56081c707bee6a58dc1960a59c9511d6fb5dfce8beb6b34713ee777d1b2169e`  
		Last Modified: Tue, 04 Feb 2025 19:33:04 GMT  
		Size: 19.6 KB (19600 bytes)  
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
$ docker pull dart@sha256:d30a0e827230c3419f90022fb821ba69c96d3b1ab98b0914aa983f3950617399
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
$ docker pull dart@sha256:553d8f8fc187ab31ad8f8ed9c4722c812057607e10a7dc5d4bb7d7e89def2c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312140840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3495d6c4d34ccf3d7457b9ecdfc1cc526891f9f4f09e260924d7e9915832923`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5a2953ec76c8139cd73d0c0b482de26d0b86a5a7e37579167bbd33493063408d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=fb06585de5d9b2aacbf8970be69c91292b29b4dab315b84789f0fe528675ae16;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f475db0944922d9925b4a4266c31f8fafd39b01a3cc130422e785c8276eb13e5;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0785300a74e92d61d24e3d60a87edaff62d5ede8e74f2e8368f0c52408c49cee`  
		Last Modified: Tue, 04 Feb 2025 19:33:06 GMT  
		Size: 54.9 MB (54906742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9859598bb5e58e0449dd2866c56d84cc61eb6220a6b0508aa6717600b468fda`  
		Last Modified: Tue, 04 Feb 2025 19:33:05 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca07202c9e54f4fe2ceb63a5856929c2c74bd045a48581925abbaa393f8bba`  
		Last Modified: Tue, 04 Feb 2025 19:33:10 GMT  
		Size: 227.2 MB (227224845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1ce94f4cc12a1678ea21e42b3970f8b3f1723599e5fd7ef168d772be9205601c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed10b94ea5d6396292c54f541f7004b4390ccf05184e6229a761784f235ff72`

```dockerfile
```

-	Layers:
	-	`sha256:e56081c707bee6a58dc1960a59c9511d6fb5dfce8beb6b34713ee777d1b2169e`  
		Last Modified: Tue, 04 Feb 2025 19:33:04 GMT  
		Size: 19.6 KB (19600 bytes)  
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
