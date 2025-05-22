<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.8`](#dart38)
-	[`dart:3.8-sdk`](#dart38-sdk)
-	[`dart:3.8.0`](#dart380)
-	[`dart:3.8.0-sdk`](#dart380-sdk)
-	[`dart:3.9.0-100.2.beta`](#dart390-1002beta)
-	[`dart:3.9.0-100.2.beta-sdk`](#dart390-1002beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:132fea97bf17a4e50202ebf282f29f0e798f269ffd2d03f5179dec066727f676
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
$ docker pull dart@sha256:2222e19c4919c213d31671d9520638bd2145a2309d830320345911677c088a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285788537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05343bcf107420ac814ade4895850bcfb53ada10cd2c9aa3d63c277312fc130`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7123238830b26d9d6f99d0a307a767f7e574ae279f3a5f5fcb59c83485ab33a0`  
		Last Modified: Wed, 21 May 2025 23:21:47 GMT  
		Size: 54.9 MB (54910399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97d53a7f96d3af27752768f441d35a380a4998932a993de3673dc02066a66db`  
		Last Modified: Wed, 21 May 2025 23:21:45 GMT  
		Size: 1.8 MB (1785450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f699c90a02cbcec5f1358e98ed290d3eb3c4800e5b101d3ade8040123a2ae138`  
		Last Modified: Wed, 21 May 2025 23:21:52 GMT  
		Size: 200.9 MB (200867326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:2116c2c5d77e64cb7d5752d5f671e0385c901740da309541171e4a5f9472f502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f51ff8a0c44b7e80fa66fd729a71b2386351eb569300f69f71f21e21a549d5`

```dockerfile
```

-	Layers:
	-	`sha256:3b701385ae480c2a18be93ead4c5700cc1bdbf922f8e2ade08a02dc5a5aab5fa`  
		Last Modified: Wed, 21 May 2025 23:21:45 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:8c841c0365614a7110ea1094a170a12ad2acd9e7d01c2099a0139c7ce3dfda81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214484649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c8ddb85e40e27b040e78006f693ea720db48a3489b72b8095a1ccd8f7615d8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c85147be7637b7c2750d42cfef2af5f2b7a9b21edf1baf341d3b9ff16d0d0b`  
		Last Modified: Thu, 22 May 2025 02:37:05 GMT  
		Size: 49.6 MB (49554662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40929bf8357109c1a8d00381005b544ba68df0322b49f6d2e58998e671ea0c84`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8228dade2aae6a866cc69c1ce0d31ec35ba591e688ac2be90cbd2caaa8748dab`  
		Last Modified: Thu, 22 May 2025 02:37:08 GMT  
		Size: 139.8 MB (139775089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:80cc4ce8a404af69cae44fb4fa602974c628991835b1f6a685d6a8e5752dec31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5359819d922d2bc9ecd3cebf3669da8fff341cd348816edfc386a79e3e73af27`

```dockerfile
```

-	Layers:
	-	`sha256:74cd3f041d7288142aa9523090c8d0347a88875125fca9485c9d1109018f92b2`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b04a1e339a9297a6aa4a42d29bba0840899f8d5da1127fe14f0ab2d4c401fc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284455973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac49d57b0bfd8415a228904cde303c9460c8f8542095854f753c4dfaf5f8a4a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cdc3e6a7951a95ca3a23969c311e0f260d2d126d6c9dff5126c9c2e83e4d94`  
		Last Modified: Thu, 22 May 2025 02:54:52 GMT  
		Size: 54.7 MB (54682308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65dae3b9ea3c5d4fbe78324186a1864aa7f37d2ed0ea7d3a97878375c5d86603`  
		Last Modified: Thu, 22 May 2025 02:54:50 GMT  
		Size: 1.5 MB (1488220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2422e8d91b945786bc4d4db6f0ef8e3f2bf7b25dd0eff0ba0cec62fdc96c9fda`  
		Last Modified: Thu, 22 May 2025 02:54:55 GMT  
		Size: 200.2 MB (200220133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:e283810be4e98386f3e32049fd4b37093f1e511e6080b1851c9256ec87cf016c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d9c85b832829e5a61565f5553a60b93dcfb37f6a329aaef650e215fb76f84d`

```dockerfile
```

-	Layers:
	-	`sha256:d0f3a891a4706bed94b5fc20f33060dff370905ed11bcf882d2c5a7c19a87236`  
		Last Modified: Thu, 22 May 2025 02:54:50 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:132fea97bf17a4e50202ebf282f29f0e798f269ffd2d03f5179dec066727f676
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
$ docker pull dart@sha256:2222e19c4919c213d31671d9520638bd2145a2309d830320345911677c088a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285788537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05343bcf107420ac814ade4895850bcfb53ada10cd2c9aa3d63c277312fc130`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7123238830b26d9d6f99d0a307a767f7e574ae279f3a5f5fcb59c83485ab33a0`  
		Last Modified: Wed, 21 May 2025 23:21:47 GMT  
		Size: 54.9 MB (54910399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97d53a7f96d3af27752768f441d35a380a4998932a993de3673dc02066a66db`  
		Last Modified: Wed, 21 May 2025 23:21:45 GMT  
		Size: 1.8 MB (1785450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f699c90a02cbcec5f1358e98ed290d3eb3c4800e5b101d3ade8040123a2ae138`  
		Last Modified: Wed, 21 May 2025 23:21:52 GMT  
		Size: 200.9 MB (200867326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:2116c2c5d77e64cb7d5752d5f671e0385c901740da309541171e4a5f9472f502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f51ff8a0c44b7e80fa66fd729a71b2386351eb569300f69f71f21e21a549d5`

```dockerfile
```

-	Layers:
	-	`sha256:3b701385ae480c2a18be93ead4c5700cc1bdbf922f8e2ade08a02dc5a5aab5fa`  
		Last Modified: Wed, 21 May 2025 23:21:45 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:8c841c0365614a7110ea1094a170a12ad2acd9e7d01c2099a0139c7ce3dfda81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214484649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c8ddb85e40e27b040e78006f693ea720db48a3489b72b8095a1ccd8f7615d8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c85147be7637b7c2750d42cfef2af5f2b7a9b21edf1baf341d3b9ff16d0d0b`  
		Last Modified: Thu, 22 May 2025 02:37:05 GMT  
		Size: 49.6 MB (49554662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40929bf8357109c1a8d00381005b544ba68df0322b49f6d2e58998e671ea0c84`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8228dade2aae6a866cc69c1ce0d31ec35ba591e688ac2be90cbd2caaa8748dab`  
		Last Modified: Thu, 22 May 2025 02:37:08 GMT  
		Size: 139.8 MB (139775089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:80cc4ce8a404af69cae44fb4fa602974c628991835b1f6a685d6a8e5752dec31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5359819d922d2bc9ecd3cebf3669da8fff341cd348816edfc386a79e3e73af27`

```dockerfile
```

-	Layers:
	-	`sha256:74cd3f041d7288142aa9523090c8d0347a88875125fca9485c9d1109018f92b2`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b04a1e339a9297a6aa4a42d29bba0840899f8d5da1127fe14f0ab2d4c401fc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284455973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac49d57b0bfd8415a228904cde303c9460c8f8542095854f753c4dfaf5f8a4a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cdc3e6a7951a95ca3a23969c311e0f260d2d126d6c9dff5126c9c2e83e4d94`  
		Last Modified: Thu, 22 May 2025 02:54:52 GMT  
		Size: 54.7 MB (54682308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65dae3b9ea3c5d4fbe78324186a1864aa7f37d2ed0ea7d3a97878375c5d86603`  
		Last Modified: Thu, 22 May 2025 02:54:50 GMT  
		Size: 1.5 MB (1488220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2422e8d91b945786bc4d4db6f0ef8e3f2bf7b25dd0eff0ba0cec62fdc96c9fda`  
		Last Modified: Thu, 22 May 2025 02:54:55 GMT  
		Size: 200.2 MB (200220133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e283810be4e98386f3e32049fd4b37093f1e511e6080b1851c9256ec87cf016c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d9c85b832829e5a61565f5553a60b93dcfb37f6a329aaef650e215fb76f84d`

```dockerfile
```

-	Layers:
	-	`sha256:d0f3a891a4706bed94b5fc20f33060dff370905ed11bcf882d2c5a7c19a87236`  
		Last Modified: Thu, 22 May 2025 02:54:50 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8`

```console
$ docker pull dart@sha256:132fea97bf17a4e50202ebf282f29f0e798f269ffd2d03f5179dec066727f676
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
$ docker pull dart@sha256:2222e19c4919c213d31671d9520638bd2145a2309d830320345911677c088a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285788537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05343bcf107420ac814ade4895850bcfb53ada10cd2c9aa3d63c277312fc130`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7123238830b26d9d6f99d0a307a767f7e574ae279f3a5f5fcb59c83485ab33a0`  
		Last Modified: Wed, 21 May 2025 23:21:47 GMT  
		Size: 54.9 MB (54910399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97d53a7f96d3af27752768f441d35a380a4998932a993de3673dc02066a66db`  
		Last Modified: Wed, 21 May 2025 23:21:45 GMT  
		Size: 1.8 MB (1785450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f699c90a02cbcec5f1358e98ed290d3eb3c4800e5b101d3ade8040123a2ae138`  
		Last Modified: Wed, 21 May 2025 23:21:52 GMT  
		Size: 200.9 MB (200867326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8` - unknown; unknown

```console
$ docker pull dart@sha256:2116c2c5d77e64cb7d5752d5f671e0385c901740da309541171e4a5f9472f502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f51ff8a0c44b7e80fa66fd729a71b2386351eb569300f69f71f21e21a549d5`

```dockerfile
```

-	Layers:
	-	`sha256:3b701385ae480c2a18be93ead4c5700cc1bdbf922f8e2ade08a02dc5a5aab5fa`  
		Last Modified: Wed, 21 May 2025 23:21:45 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8` - linux; arm variant v7

```console
$ docker pull dart@sha256:8c841c0365614a7110ea1094a170a12ad2acd9e7d01c2099a0139c7ce3dfda81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214484649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c8ddb85e40e27b040e78006f693ea720db48a3489b72b8095a1ccd8f7615d8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c85147be7637b7c2750d42cfef2af5f2b7a9b21edf1baf341d3b9ff16d0d0b`  
		Last Modified: Thu, 22 May 2025 02:37:05 GMT  
		Size: 49.6 MB (49554662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40929bf8357109c1a8d00381005b544ba68df0322b49f6d2e58998e671ea0c84`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8228dade2aae6a866cc69c1ce0d31ec35ba591e688ac2be90cbd2caaa8748dab`  
		Last Modified: Thu, 22 May 2025 02:37:08 GMT  
		Size: 139.8 MB (139775089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8` - unknown; unknown

```console
$ docker pull dart@sha256:80cc4ce8a404af69cae44fb4fa602974c628991835b1f6a685d6a8e5752dec31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5359819d922d2bc9ecd3cebf3669da8fff341cd348816edfc386a79e3e73af27`

```dockerfile
```

-	Layers:
	-	`sha256:74cd3f041d7288142aa9523090c8d0347a88875125fca9485c9d1109018f92b2`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b04a1e339a9297a6aa4a42d29bba0840899f8d5da1127fe14f0ab2d4c401fc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284455973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac49d57b0bfd8415a228904cde303c9460c8f8542095854f753c4dfaf5f8a4a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cdc3e6a7951a95ca3a23969c311e0f260d2d126d6c9dff5126c9c2e83e4d94`  
		Last Modified: Thu, 22 May 2025 02:54:52 GMT  
		Size: 54.7 MB (54682308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65dae3b9ea3c5d4fbe78324186a1864aa7f37d2ed0ea7d3a97878375c5d86603`  
		Last Modified: Thu, 22 May 2025 02:54:50 GMT  
		Size: 1.5 MB (1488220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2422e8d91b945786bc4d4db6f0ef8e3f2bf7b25dd0eff0ba0cec62fdc96c9fda`  
		Last Modified: Thu, 22 May 2025 02:54:55 GMT  
		Size: 200.2 MB (200220133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8` - unknown; unknown

```console
$ docker pull dart@sha256:e283810be4e98386f3e32049fd4b37093f1e511e6080b1851c9256ec87cf016c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d9c85b832829e5a61565f5553a60b93dcfb37f6a329aaef650e215fb76f84d`

```dockerfile
```

-	Layers:
	-	`sha256:d0f3a891a4706bed94b5fc20f33060dff370905ed11bcf882d2c5a7c19a87236`  
		Last Modified: Thu, 22 May 2025 02:54:50 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8-sdk`

```console
$ docker pull dart@sha256:132fea97bf17a4e50202ebf282f29f0e798f269ffd2d03f5179dec066727f676
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
$ docker pull dart@sha256:2222e19c4919c213d31671d9520638bd2145a2309d830320345911677c088a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285788537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05343bcf107420ac814ade4895850bcfb53ada10cd2c9aa3d63c277312fc130`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7123238830b26d9d6f99d0a307a767f7e574ae279f3a5f5fcb59c83485ab33a0`  
		Last Modified: Wed, 21 May 2025 23:21:47 GMT  
		Size: 54.9 MB (54910399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97d53a7f96d3af27752768f441d35a380a4998932a993de3673dc02066a66db`  
		Last Modified: Wed, 21 May 2025 23:21:45 GMT  
		Size: 1.8 MB (1785450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f699c90a02cbcec5f1358e98ed290d3eb3c4800e5b101d3ade8040123a2ae138`  
		Last Modified: Wed, 21 May 2025 23:21:52 GMT  
		Size: 200.9 MB (200867326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:2116c2c5d77e64cb7d5752d5f671e0385c901740da309541171e4a5f9472f502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f51ff8a0c44b7e80fa66fd729a71b2386351eb569300f69f71f21e21a549d5`

```dockerfile
```

-	Layers:
	-	`sha256:3b701385ae480c2a18be93ead4c5700cc1bdbf922f8e2ade08a02dc5a5aab5fa`  
		Last Modified: Wed, 21 May 2025 23:21:45 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:8c841c0365614a7110ea1094a170a12ad2acd9e7d01c2099a0139c7ce3dfda81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214484649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c8ddb85e40e27b040e78006f693ea720db48a3489b72b8095a1ccd8f7615d8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c85147be7637b7c2750d42cfef2af5f2b7a9b21edf1baf341d3b9ff16d0d0b`  
		Last Modified: Thu, 22 May 2025 02:37:05 GMT  
		Size: 49.6 MB (49554662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40929bf8357109c1a8d00381005b544ba68df0322b49f6d2e58998e671ea0c84`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8228dade2aae6a866cc69c1ce0d31ec35ba591e688ac2be90cbd2caaa8748dab`  
		Last Modified: Thu, 22 May 2025 02:37:08 GMT  
		Size: 139.8 MB (139775089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:80cc4ce8a404af69cae44fb4fa602974c628991835b1f6a685d6a8e5752dec31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5359819d922d2bc9ecd3cebf3669da8fff341cd348816edfc386a79e3e73af27`

```dockerfile
```

-	Layers:
	-	`sha256:74cd3f041d7288142aa9523090c8d0347a88875125fca9485c9d1109018f92b2`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b04a1e339a9297a6aa4a42d29bba0840899f8d5da1127fe14f0ab2d4c401fc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284455973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac49d57b0bfd8415a228904cde303c9460c8f8542095854f753c4dfaf5f8a4a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cdc3e6a7951a95ca3a23969c311e0f260d2d126d6c9dff5126c9c2e83e4d94`  
		Last Modified: Thu, 22 May 2025 02:54:52 GMT  
		Size: 54.7 MB (54682308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65dae3b9ea3c5d4fbe78324186a1864aa7f37d2ed0ea7d3a97878375c5d86603`  
		Last Modified: Thu, 22 May 2025 02:54:50 GMT  
		Size: 1.5 MB (1488220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2422e8d91b945786bc4d4db6f0ef8e3f2bf7b25dd0eff0ba0cec62fdc96c9fda`  
		Last Modified: Thu, 22 May 2025 02:54:55 GMT  
		Size: 200.2 MB (200220133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e283810be4e98386f3e32049fd4b37093f1e511e6080b1851c9256ec87cf016c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d9c85b832829e5a61565f5553a60b93dcfb37f6a329aaef650e215fb76f84d`

```dockerfile
```

-	Layers:
	-	`sha256:d0f3a891a4706bed94b5fc20f33060dff370905ed11bcf882d2c5a7c19a87236`  
		Last Modified: Thu, 22 May 2025 02:54:50 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8.0`

```console
$ docker pull dart@sha256:132fea97bf17a4e50202ebf282f29f0e798f269ffd2d03f5179dec066727f676
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.8.0` - linux; amd64

```console
$ docker pull dart@sha256:2222e19c4919c213d31671d9520638bd2145a2309d830320345911677c088a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285788537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05343bcf107420ac814ade4895850bcfb53ada10cd2c9aa3d63c277312fc130`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7123238830b26d9d6f99d0a307a767f7e574ae279f3a5f5fcb59c83485ab33a0`  
		Last Modified: Wed, 21 May 2025 23:21:47 GMT  
		Size: 54.9 MB (54910399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97d53a7f96d3af27752768f441d35a380a4998932a993de3673dc02066a66db`  
		Last Modified: Wed, 21 May 2025 23:21:45 GMT  
		Size: 1.8 MB (1785450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f699c90a02cbcec5f1358e98ed290d3eb3c4800e5b101d3ade8040123a2ae138`  
		Last Modified: Wed, 21 May 2025 23:21:52 GMT  
		Size: 200.9 MB (200867326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0` - unknown; unknown

```console
$ docker pull dart@sha256:2116c2c5d77e64cb7d5752d5f671e0385c901740da309541171e4a5f9472f502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f51ff8a0c44b7e80fa66fd729a71b2386351eb569300f69f71f21e21a549d5`

```dockerfile
```

-	Layers:
	-	`sha256:3b701385ae480c2a18be93ead4c5700cc1bdbf922f8e2ade08a02dc5a5aab5fa`  
		Last Modified: Wed, 21 May 2025 23:21:45 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.0` - linux; arm variant v7

```console
$ docker pull dart@sha256:8c841c0365614a7110ea1094a170a12ad2acd9e7d01c2099a0139c7ce3dfda81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214484649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c8ddb85e40e27b040e78006f693ea720db48a3489b72b8095a1ccd8f7615d8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c85147be7637b7c2750d42cfef2af5f2b7a9b21edf1baf341d3b9ff16d0d0b`  
		Last Modified: Thu, 22 May 2025 02:37:05 GMT  
		Size: 49.6 MB (49554662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40929bf8357109c1a8d00381005b544ba68df0322b49f6d2e58998e671ea0c84`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8228dade2aae6a866cc69c1ce0d31ec35ba591e688ac2be90cbd2caaa8748dab`  
		Last Modified: Thu, 22 May 2025 02:37:08 GMT  
		Size: 139.8 MB (139775089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0` - unknown; unknown

```console
$ docker pull dart@sha256:80cc4ce8a404af69cae44fb4fa602974c628991835b1f6a685d6a8e5752dec31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5359819d922d2bc9ecd3cebf3669da8fff341cd348816edfc386a79e3e73af27`

```dockerfile
```

-	Layers:
	-	`sha256:74cd3f041d7288142aa9523090c8d0347a88875125fca9485c9d1109018f92b2`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.0` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b04a1e339a9297a6aa4a42d29bba0840899f8d5da1127fe14f0ab2d4c401fc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284455973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac49d57b0bfd8415a228904cde303c9460c8f8542095854f753c4dfaf5f8a4a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cdc3e6a7951a95ca3a23969c311e0f260d2d126d6c9dff5126c9c2e83e4d94`  
		Last Modified: Thu, 22 May 2025 02:54:52 GMT  
		Size: 54.7 MB (54682308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65dae3b9ea3c5d4fbe78324186a1864aa7f37d2ed0ea7d3a97878375c5d86603`  
		Last Modified: Thu, 22 May 2025 02:54:50 GMT  
		Size: 1.5 MB (1488220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2422e8d91b945786bc4d4db6f0ef8e3f2bf7b25dd0eff0ba0cec62fdc96c9fda`  
		Last Modified: Thu, 22 May 2025 02:54:55 GMT  
		Size: 200.2 MB (200220133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0` - unknown; unknown

```console
$ docker pull dart@sha256:e283810be4e98386f3e32049fd4b37093f1e511e6080b1851c9256ec87cf016c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d9c85b832829e5a61565f5553a60b93dcfb37f6a329aaef650e215fb76f84d`

```dockerfile
```

-	Layers:
	-	`sha256:d0f3a891a4706bed94b5fc20f33060dff370905ed11bcf882d2c5a7c19a87236`  
		Last Modified: Thu, 22 May 2025 02:54:50 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8.0-sdk`

```console
$ docker pull dart@sha256:132fea97bf17a4e50202ebf282f29f0e798f269ffd2d03f5179dec066727f676
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.8.0-sdk` - linux; amd64

```console
$ docker pull dart@sha256:2222e19c4919c213d31671d9520638bd2145a2309d830320345911677c088a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285788537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05343bcf107420ac814ade4895850bcfb53ada10cd2c9aa3d63c277312fc130`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7123238830b26d9d6f99d0a307a767f7e574ae279f3a5f5fcb59c83485ab33a0`  
		Last Modified: Wed, 21 May 2025 23:21:47 GMT  
		Size: 54.9 MB (54910399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97d53a7f96d3af27752768f441d35a380a4998932a993de3673dc02066a66db`  
		Last Modified: Wed, 21 May 2025 23:21:45 GMT  
		Size: 1.8 MB (1785450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f699c90a02cbcec5f1358e98ed290d3eb3c4800e5b101d3ade8040123a2ae138`  
		Last Modified: Wed, 21 May 2025 23:21:52 GMT  
		Size: 200.9 MB (200867326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:2116c2c5d77e64cb7d5752d5f671e0385c901740da309541171e4a5f9472f502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f51ff8a0c44b7e80fa66fd729a71b2386351eb569300f69f71f21e21a549d5`

```dockerfile
```

-	Layers:
	-	`sha256:3b701385ae480c2a18be93ead4c5700cc1bdbf922f8e2ade08a02dc5a5aab5fa`  
		Last Modified: Wed, 21 May 2025 23:21:45 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.0-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:8c841c0365614a7110ea1094a170a12ad2acd9e7d01c2099a0139c7ce3dfda81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214484649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c8ddb85e40e27b040e78006f693ea720db48a3489b72b8095a1ccd8f7615d8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c85147be7637b7c2750d42cfef2af5f2b7a9b21edf1baf341d3b9ff16d0d0b`  
		Last Modified: Thu, 22 May 2025 02:37:05 GMT  
		Size: 49.6 MB (49554662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40929bf8357109c1a8d00381005b544ba68df0322b49f6d2e58998e671ea0c84`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8228dade2aae6a866cc69c1ce0d31ec35ba591e688ac2be90cbd2caaa8748dab`  
		Last Modified: Thu, 22 May 2025 02:37:08 GMT  
		Size: 139.8 MB (139775089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:80cc4ce8a404af69cae44fb4fa602974c628991835b1f6a685d6a8e5752dec31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5359819d922d2bc9ecd3cebf3669da8fff341cd348816edfc386a79e3e73af27`

```dockerfile
```

-	Layers:
	-	`sha256:74cd3f041d7288142aa9523090c8d0347a88875125fca9485c9d1109018f92b2`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.0-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b04a1e339a9297a6aa4a42d29bba0840899f8d5da1127fe14f0ab2d4c401fc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284455973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac49d57b0bfd8415a228904cde303c9460c8f8542095854f753c4dfaf5f8a4a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cdc3e6a7951a95ca3a23969c311e0f260d2d126d6c9dff5126c9c2e83e4d94`  
		Last Modified: Thu, 22 May 2025 02:54:52 GMT  
		Size: 54.7 MB (54682308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65dae3b9ea3c5d4fbe78324186a1864aa7f37d2ed0ea7d3a97878375c5d86603`  
		Last Modified: Thu, 22 May 2025 02:54:50 GMT  
		Size: 1.5 MB (1488220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2422e8d91b945786bc4d4db6f0ef8e3f2bf7b25dd0eff0ba0cec62fdc96c9fda`  
		Last Modified: Thu, 22 May 2025 02:54:55 GMT  
		Size: 200.2 MB (200220133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e283810be4e98386f3e32049fd4b37093f1e511e6080b1851c9256ec87cf016c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d9c85b832829e5a61565f5553a60b93dcfb37f6a329aaef650e215fb76f84d`

```dockerfile
```

-	Layers:
	-	`sha256:d0f3a891a4706bed94b5fc20f33060dff370905ed11bcf882d2c5a7c19a87236`  
		Last Modified: Thu, 22 May 2025 02:54:50 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9.0-100.2.beta`

```console
$ docker pull dart@sha256:66489fe773c404431290502d2cd60e0211160f6a0b0de786c565cd417d672a2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.9.0-100.2.beta` - linux; amd64

```console
$ docker pull dart@sha256:8b2e8dfe4518fbe9e67d26526701b4f8d34c95ed329caa5b910f013f7ac38826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299684128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81eb3ae80660606c11d78657f0daad75a8565ec606fe9d6264c472e92b267e34`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb0a4507c9ee778e2e7fe8b0fd36061bda9b5b37be4892e1f7e26ae64ca63cd`  
		Last Modified: Wed, 21 May 2025 23:21:40 GMT  
		Size: 54.9 MB (54910275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4377ea873cd754a6a20978f50996cd442a5a656557176945efe2a8b512c8ec67`  
		Last Modified: Wed, 21 May 2025 23:21:39 GMT  
		Size: 1.8 MB (1785446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0b5658be57652ba42697ef25b7a9fcbfdc40cbe1eeeb11544166e1fa153bd9`  
		Last Modified: Wed, 21 May 2025 23:21:43 GMT  
		Size: 214.8 MB (214763045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-100.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:57bb63a6f945d0fdf4b08888b1d0edbf0f243e17dfea9d07ccd8722a9802fe69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb00aa04bf21daef47629493fe69ebaba48417832b96f54c57be7e9b1e1981d`

```dockerfile
```

-	Layers:
	-	`sha256:b4acf42fdf38ffa5f72d16502b4159a55abdc7a254940dad6aef18b6ba08ebbe`  
		Last Modified: Wed, 21 May 2025 23:21:39 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.0-100.2.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:03a3b7b47326962209f87beeacd3eb2beb77ae1a58147c294437796b564a0c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223850960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea0415e30900574f17287de1bf08ed29754670482974ceb0ef47156da3903e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c85147be7637b7c2750d42cfef2af5f2b7a9b21edf1baf341d3b9ff16d0d0b`  
		Last Modified: Thu, 22 May 2025 02:37:05 GMT  
		Size: 49.6 MB (49554662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40929bf8357109c1a8d00381005b544ba68df0322b49f6d2e58998e671ea0c84`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e674a4e954f37a2bea7b39bb7bb33f0526ff54a763b6f563b9717ee1a01bcf36`  
		Last Modified: Thu, 22 May 2025 02:38:00 GMT  
		Size: 149.1 MB (149141400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-100.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:ab6333dc024d7ceab9fc6de6dedcccb1a761752efd73d4821f25be1930a5068d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847a17d042ccd5aff4eb4fab301da9b1c6bf85409ce308354c661871063aba0b`

```dockerfile
```

-	Layers:
	-	`sha256:5a1ae61141b68903af3af9a9e6523ba36f73d56da8b962383e0900856e083d1f`  
		Last Modified: Thu, 22 May 2025 02:37:55 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.0-100.2.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0cd5e15325a895087d8d0a9680d5020a75865954b678fd23b6e50890e6da57d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298384382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9793712575419414a0b91a392b076824d7c037fca5673686a82a1e0c2ced825d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4e386db6cc4700dfab329e9817bf54f58b0793d4429d1d34a2ea344a1d2d43`  
		Last Modified: Thu, 22 May 2025 08:19:57 GMT  
		Size: 54.7 MB (54682805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0fdc18782299615847c130f05a333ae7ff5df5aa327b4c5e585b3592d2212f`  
		Last Modified: Thu, 22 May 2025 08:19:55 GMT  
		Size: 1.5 MB (1488212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce4953d9d9148ba328eb4570971c9a32bb08d3794bcf6dd6e255605e1d1ad30`  
		Last Modified: Thu, 22 May 2025 08:20:00 GMT  
		Size: 214.1 MB (214148053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-100.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:1e423facc53e25464ea0ab09e9070c64cbf3ba353e6668db9a690ef724ceb24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108dd0f99ab6cde3c9a98a846f04cd6b57ab573b70aef98278eafff83619ccd2`

```dockerfile
```

-	Layers:
	-	`sha256:e9638a2b32d865f861bd8de2bd4518a8a598e12e80d71f0b149bc2be3a62c275`  
		Last Modified: Thu, 22 May 2025 08:19:55 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9.0-100.2.beta-sdk`

```console
$ docker pull dart@sha256:66489fe773c404431290502d2cd60e0211160f6a0b0de786c565cd417d672a2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.9.0-100.2.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:8b2e8dfe4518fbe9e67d26526701b4f8d34c95ed329caa5b910f013f7ac38826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299684128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81eb3ae80660606c11d78657f0daad75a8565ec606fe9d6264c472e92b267e34`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb0a4507c9ee778e2e7fe8b0fd36061bda9b5b37be4892e1f7e26ae64ca63cd`  
		Last Modified: Wed, 21 May 2025 23:21:40 GMT  
		Size: 54.9 MB (54910275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4377ea873cd754a6a20978f50996cd442a5a656557176945efe2a8b512c8ec67`  
		Last Modified: Wed, 21 May 2025 23:21:39 GMT  
		Size: 1.8 MB (1785446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0b5658be57652ba42697ef25b7a9fcbfdc40cbe1eeeb11544166e1fa153bd9`  
		Last Modified: Wed, 21 May 2025 23:21:43 GMT  
		Size: 214.8 MB (214763045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-100.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:57bb63a6f945d0fdf4b08888b1d0edbf0f243e17dfea9d07ccd8722a9802fe69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb00aa04bf21daef47629493fe69ebaba48417832b96f54c57be7e9b1e1981d`

```dockerfile
```

-	Layers:
	-	`sha256:b4acf42fdf38ffa5f72d16502b4159a55abdc7a254940dad6aef18b6ba08ebbe`  
		Last Modified: Wed, 21 May 2025 23:21:39 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.0-100.2.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:03a3b7b47326962209f87beeacd3eb2beb77ae1a58147c294437796b564a0c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223850960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea0415e30900574f17287de1bf08ed29754670482974ceb0ef47156da3903e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c85147be7637b7c2750d42cfef2af5f2b7a9b21edf1baf341d3b9ff16d0d0b`  
		Last Modified: Thu, 22 May 2025 02:37:05 GMT  
		Size: 49.6 MB (49554662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40929bf8357109c1a8d00381005b544ba68df0322b49f6d2e58998e671ea0c84`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e674a4e954f37a2bea7b39bb7bb33f0526ff54a763b6f563b9717ee1a01bcf36`  
		Last Modified: Thu, 22 May 2025 02:38:00 GMT  
		Size: 149.1 MB (149141400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-100.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ab6333dc024d7ceab9fc6de6dedcccb1a761752efd73d4821f25be1930a5068d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847a17d042ccd5aff4eb4fab301da9b1c6bf85409ce308354c661871063aba0b`

```dockerfile
```

-	Layers:
	-	`sha256:5a1ae61141b68903af3af9a9e6523ba36f73d56da8b962383e0900856e083d1f`  
		Last Modified: Thu, 22 May 2025 02:37:55 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.0-100.2.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0cd5e15325a895087d8d0a9680d5020a75865954b678fd23b6e50890e6da57d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298384382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9793712575419414a0b91a392b076824d7c037fca5673686a82a1e0c2ced825d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4e386db6cc4700dfab329e9817bf54f58b0793d4429d1d34a2ea344a1d2d43`  
		Last Modified: Thu, 22 May 2025 08:19:57 GMT  
		Size: 54.7 MB (54682805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0fdc18782299615847c130f05a333ae7ff5df5aa327b4c5e585b3592d2212f`  
		Last Modified: Thu, 22 May 2025 08:19:55 GMT  
		Size: 1.5 MB (1488212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce4953d9d9148ba328eb4570971c9a32bb08d3794bcf6dd6e255605e1d1ad30`  
		Last Modified: Thu, 22 May 2025 08:20:00 GMT  
		Size: 214.1 MB (214148053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-100.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1e423facc53e25464ea0ab09e9070c64cbf3ba353e6668db9a690ef724ceb24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108dd0f99ab6cde3c9a98a846f04cd6b57ab573b70aef98278eafff83619ccd2`

```dockerfile
```

-	Layers:
	-	`sha256:e9638a2b32d865f861bd8de2bd4518a8a598e12e80d71f0b149bc2be3a62c275`  
		Last Modified: Thu, 22 May 2025 08:19:55 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:66489fe773c404431290502d2cd60e0211160f6a0b0de786c565cd417d672a2b
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
$ docker pull dart@sha256:8b2e8dfe4518fbe9e67d26526701b4f8d34c95ed329caa5b910f013f7ac38826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299684128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81eb3ae80660606c11d78657f0daad75a8565ec606fe9d6264c472e92b267e34`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb0a4507c9ee778e2e7fe8b0fd36061bda9b5b37be4892e1f7e26ae64ca63cd`  
		Last Modified: Wed, 21 May 2025 23:21:40 GMT  
		Size: 54.9 MB (54910275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4377ea873cd754a6a20978f50996cd442a5a656557176945efe2a8b512c8ec67`  
		Last Modified: Wed, 21 May 2025 23:21:39 GMT  
		Size: 1.8 MB (1785446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0b5658be57652ba42697ef25b7a9fcbfdc40cbe1eeeb11544166e1fa153bd9`  
		Last Modified: Wed, 21 May 2025 23:21:43 GMT  
		Size: 214.8 MB (214763045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:57bb63a6f945d0fdf4b08888b1d0edbf0f243e17dfea9d07ccd8722a9802fe69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb00aa04bf21daef47629493fe69ebaba48417832b96f54c57be7e9b1e1981d`

```dockerfile
```

-	Layers:
	-	`sha256:b4acf42fdf38ffa5f72d16502b4159a55abdc7a254940dad6aef18b6ba08ebbe`  
		Last Modified: Wed, 21 May 2025 23:21:39 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:03a3b7b47326962209f87beeacd3eb2beb77ae1a58147c294437796b564a0c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223850960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea0415e30900574f17287de1bf08ed29754670482974ceb0ef47156da3903e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c85147be7637b7c2750d42cfef2af5f2b7a9b21edf1baf341d3b9ff16d0d0b`  
		Last Modified: Thu, 22 May 2025 02:37:05 GMT  
		Size: 49.6 MB (49554662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40929bf8357109c1a8d00381005b544ba68df0322b49f6d2e58998e671ea0c84`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e674a4e954f37a2bea7b39bb7bb33f0526ff54a763b6f563b9717ee1a01bcf36`  
		Last Modified: Thu, 22 May 2025 02:38:00 GMT  
		Size: 149.1 MB (149141400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:ab6333dc024d7ceab9fc6de6dedcccb1a761752efd73d4821f25be1930a5068d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847a17d042ccd5aff4eb4fab301da9b1c6bf85409ce308354c661871063aba0b`

```dockerfile
```

-	Layers:
	-	`sha256:5a1ae61141b68903af3af9a9e6523ba36f73d56da8b962383e0900856e083d1f`  
		Last Modified: Thu, 22 May 2025 02:37:55 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0cd5e15325a895087d8d0a9680d5020a75865954b678fd23b6e50890e6da57d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298384382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9793712575419414a0b91a392b076824d7c037fca5673686a82a1e0c2ced825d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4e386db6cc4700dfab329e9817bf54f58b0793d4429d1d34a2ea344a1d2d43`  
		Last Modified: Thu, 22 May 2025 08:19:57 GMT  
		Size: 54.7 MB (54682805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0fdc18782299615847c130f05a333ae7ff5df5aa327b4c5e585b3592d2212f`  
		Last Modified: Thu, 22 May 2025 08:19:55 GMT  
		Size: 1.5 MB (1488212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce4953d9d9148ba328eb4570971c9a32bb08d3794bcf6dd6e255605e1d1ad30`  
		Last Modified: Thu, 22 May 2025 08:20:00 GMT  
		Size: 214.1 MB (214148053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:1e423facc53e25464ea0ab09e9070c64cbf3ba353e6668db9a690ef724ceb24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108dd0f99ab6cde3c9a98a846f04cd6b57ab573b70aef98278eafff83619ccd2`

```dockerfile
```

-	Layers:
	-	`sha256:e9638a2b32d865f861bd8de2bd4518a8a598e12e80d71f0b149bc2be3a62c275`  
		Last Modified: Thu, 22 May 2025 08:19:55 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:66489fe773c404431290502d2cd60e0211160f6a0b0de786c565cd417d672a2b
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
$ docker pull dart@sha256:8b2e8dfe4518fbe9e67d26526701b4f8d34c95ed329caa5b910f013f7ac38826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299684128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81eb3ae80660606c11d78657f0daad75a8565ec606fe9d6264c472e92b267e34`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb0a4507c9ee778e2e7fe8b0fd36061bda9b5b37be4892e1f7e26ae64ca63cd`  
		Last Modified: Wed, 21 May 2025 23:21:40 GMT  
		Size: 54.9 MB (54910275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4377ea873cd754a6a20978f50996cd442a5a656557176945efe2a8b512c8ec67`  
		Last Modified: Wed, 21 May 2025 23:21:39 GMT  
		Size: 1.8 MB (1785446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0b5658be57652ba42697ef25b7a9fcbfdc40cbe1eeeb11544166e1fa153bd9`  
		Last Modified: Wed, 21 May 2025 23:21:43 GMT  
		Size: 214.8 MB (214763045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:57bb63a6f945d0fdf4b08888b1d0edbf0f243e17dfea9d07ccd8722a9802fe69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb00aa04bf21daef47629493fe69ebaba48417832b96f54c57be7e9b1e1981d`

```dockerfile
```

-	Layers:
	-	`sha256:b4acf42fdf38ffa5f72d16502b4159a55abdc7a254940dad6aef18b6ba08ebbe`  
		Last Modified: Wed, 21 May 2025 23:21:39 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:03a3b7b47326962209f87beeacd3eb2beb77ae1a58147c294437796b564a0c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223850960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea0415e30900574f17287de1bf08ed29754670482974ceb0ef47156da3903e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c85147be7637b7c2750d42cfef2af5f2b7a9b21edf1baf341d3b9ff16d0d0b`  
		Last Modified: Thu, 22 May 2025 02:37:05 GMT  
		Size: 49.6 MB (49554662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40929bf8357109c1a8d00381005b544ba68df0322b49f6d2e58998e671ea0c84`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e674a4e954f37a2bea7b39bb7bb33f0526ff54a763b6f563b9717ee1a01bcf36`  
		Last Modified: Thu, 22 May 2025 02:38:00 GMT  
		Size: 149.1 MB (149141400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ab6333dc024d7ceab9fc6de6dedcccb1a761752efd73d4821f25be1930a5068d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847a17d042ccd5aff4eb4fab301da9b1c6bf85409ce308354c661871063aba0b`

```dockerfile
```

-	Layers:
	-	`sha256:5a1ae61141b68903af3af9a9e6523ba36f73d56da8b962383e0900856e083d1f`  
		Last Modified: Thu, 22 May 2025 02:37:55 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0cd5e15325a895087d8d0a9680d5020a75865954b678fd23b6e50890e6da57d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298384382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9793712575419414a0b91a392b076824d7c037fca5673686a82a1e0c2ced825d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4e386db6cc4700dfab329e9817bf54f58b0793d4429d1d34a2ea344a1d2d43`  
		Last Modified: Thu, 22 May 2025 08:19:57 GMT  
		Size: 54.7 MB (54682805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0fdc18782299615847c130f05a333ae7ff5df5aa327b4c5e585b3592d2212f`  
		Last Modified: Thu, 22 May 2025 08:19:55 GMT  
		Size: 1.5 MB (1488212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce4953d9d9148ba328eb4570971c9a32bb08d3794bcf6dd6e255605e1d1ad30`  
		Last Modified: Thu, 22 May 2025 08:20:00 GMT  
		Size: 214.1 MB (214148053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1e423facc53e25464ea0ab09e9070c64cbf3ba353e6668db9a690ef724ceb24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108dd0f99ab6cde3c9a98a846f04cd6b57ab573b70aef98278eafff83619ccd2`

```dockerfile
```

-	Layers:
	-	`sha256:e9638a2b32d865f861bd8de2bd4518a8a598e12e80d71f0b149bc2be3a62c275`  
		Last Modified: Thu, 22 May 2025 08:19:55 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:132fea97bf17a4e50202ebf282f29f0e798f269ffd2d03f5179dec066727f676
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
$ docker pull dart@sha256:2222e19c4919c213d31671d9520638bd2145a2309d830320345911677c088a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285788537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05343bcf107420ac814ade4895850bcfb53ada10cd2c9aa3d63c277312fc130`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7123238830b26d9d6f99d0a307a767f7e574ae279f3a5f5fcb59c83485ab33a0`  
		Last Modified: Wed, 21 May 2025 23:21:47 GMT  
		Size: 54.9 MB (54910399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97d53a7f96d3af27752768f441d35a380a4998932a993de3673dc02066a66db`  
		Last Modified: Wed, 21 May 2025 23:21:45 GMT  
		Size: 1.8 MB (1785450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f699c90a02cbcec5f1358e98ed290d3eb3c4800e5b101d3ade8040123a2ae138`  
		Last Modified: Wed, 21 May 2025 23:21:52 GMT  
		Size: 200.9 MB (200867326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:2116c2c5d77e64cb7d5752d5f671e0385c901740da309541171e4a5f9472f502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f51ff8a0c44b7e80fa66fd729a71b2386351eb569300f69f71f21e21a549d5`

```dockerfile
```

-	Layers:
	-	`sha256:3b701385ae480c2a18be93ead4c5700cc1bdbf922f8e2ade08a02dc5a5aab5fa`  
		Last Modified: Wed, 21 May 2025 23:21:45 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:8c841c0365614a7110ea1094a170a12ad2acd9e7d01c2099a0139c7ce3dfda81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214484649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c8ddb85e40e27b040e78006f693ea720db48a3489b72b8095a1ccd8f7615d8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c85147be7637b7c2750d42cfef2af5f2b7a9b21edf1baf341d3b9ff16d0d0b`  
		Last Modified: Thu, 22 May 2025 02:37:05 GMT  
		Size: 49.6 MB (49554662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40929bf8357109c1a8d00381005b544ba68df0322b49f6d2e58998e671ea0c84`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8228dade2aae6a866cc69c1ce0d31ec35ba591e688ac2be90cbd2caaa8748dab`  
		Last Modified: Thu, 22 May 2025 02:37:08 GMT  
		Size: 139.8 MB (139775089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:80cc4ce8a404af69cae44fb4fa602974c628991835b1f6a685d6a8e5752dec31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5359819d922d2bc9ecd3cebf3669da8fff341cd348816edfc386a79e3e73af27`

```dockerfile
```

-	Layers:
	-	`sha256:74cd3f041d7288142aa9523090c8d0347a88875125fca9485c9d1109018f92b2`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b04a1e339a9297a6aa4a42d29bba0840899f8d5da1127fe14f0ab2d4c401fc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284455973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac49d57b0bfd8415a228904cde303c9460c8f8542095854f753c4dfaf5f8a4a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cdc3e6a7951a95ca3a23969c311e0f260d2d126d6c9dff5126c9c2e83e4d94`  
		Last Modified: Thu, 22 May 2025 02:54:52 GMT  
		Size: 54.7 MB (54682308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65dae3b9ea3c5d4fbe78324186a1864aa7f37d2ed0ea7d3a97878375c5d86603`  
		Last Modified: Thu, 22 May 2025 02:54:50 GMT  
		Size: 1.5 MB (1488220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2422e8d91b945786bc4d4db6f0ef8e3f2bf7b25dd0eff0ba0cec62fdc96c9fda`  
		Last Modified: Thu, 22 May 2025 02:54:55 GMT  
		Size: 200.2 MB (200220133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:e283810be4e98386f3e32049fd4b37093f1e511e6080b1851c9256ec87cf016c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d9c85b832829e5a61565f5553a60b93dcfb37f6a329aaef650e215fb76f84d`

```dockerfile
```

-	Layers:
	-	`sha256:d0f3a891a4706bed94b5fc20f33060dff370905ed11bcf882d2c5a7c19a87236`  
		Last Modified: Thu, 22 May 2025 02:54:50 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:132fea97bf17a4e50202ebf282f29f0e798f269ffd2d03f5179dec066727f676
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
$ docker pull dart@sha256:2222e19c4919c213d31671d9520638bd2145a2309d830320345911677c088a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285788537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05343bcf107420ac814ade4895850bcfb53ada10cd2c9aa3d63c277312fc130`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7123238830b26d9d6f99d0a307a767f7e574ae279f3a5f5fcb59c83485ab33a0`  
		Last Modified: Wed, 21 May 2025 23:21:47 GMT  
		Size: 54.9 MB (54910399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97d53a7f96d3af27752768f441d35a380a4998932a993de3673dc02066a66db`  
		Last Modified: Wed, 21 May 2025 23:21:45 GMT  
		Size: 1.8 MB (1785450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f699c90a02cbcec5f1358e98ed290d3eb3c4800e5b101d3ade8040123a2ae138`  
		Last Modified: Wed, 21 May 2025 23:21:52 GMT  
		Size: 200.9 MB (200867326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:2116c2c5d77e64cb7d5752d5f671e0385c901740da309541171e4a5f9472f502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f51ff8a0c44b7e80fa66fd729a71b2386351eb569300f69f71f21e21a549d5`

```dockerfile
```

-	Layers:
	-	`sha256:3b701385ae480c2a18be93ead4c5700cc1bdbf922f8e2ade08a02dc5a5aab5fa`  
		Last Modified: Wed, 21 May 2025 23:21:45 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:8c841c0365614a7110ea1094a170a12ad2acd9e7d01c2099a0139c7ce3dfda81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214484649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c8ddb85e40e27b040e78006f693ea720db48a3489b72b8095a1ccd8f7615d8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c85147be7637b7c2750d42cfef2af5f2b7a9b21edf1baf341d3b9ff16d0d0b`  
		Last Modified: Thu, 22 May 2025 02:37:05 GMT  
		Size: 49.6 MB (49554662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40929bf8357109c1a8d00381005b544ba68df0322b49f6d2e58998e671ea0c84`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8228dade2aae6a866cc69c1ce0d31ec35ba591e688ac2be90cbd2caaa8748dab`  
		Last Modified: Thu, 22 May 2025 02:37:08 GMT  
		Size: 139.8 MB (139775089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:80cc4ce8a404af69cae44fb4fa602974c628991835b1f6a685d6a8e5752dec31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5359819d922d2bc9ecd3cebf3669da8fff341cd348816edfc386a79e3e73af27`

```dockerfile
```

-	Layers:
	-	`sha256:74cd3f041d7288142aa9523090c8d0347a88875125fca9485c9d1109018f92b2`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b04a1e339a9297a6aa4a42d29bba0840899f8d5da1127fe14f0ab2d4c401fc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284455973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac49d57b0bfd8415a228904cde303c9460c8f8542095854f753c4dfaf5f8a4a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cdc3e6a7951a95ca3a23969c311e0f260d2d126d6c9dff5126c9c2e83e4d94`  
		Last Modified: Thu, 22 May 2025 02:54:52 GMT  
		Size: 54.7 MB (54682308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65dae3b9ea3c5d4fbe78324186a1864aa7f37d2ed0ea7d3a97878375c5d86603`  
		Last Modified: Thu, 22 May 2025 02:54:50 GMT  
		Size: 1.5 MB (1488220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2422e8d91b945786bc4d4db6f0ef8e3f2bf7b25dd0eff0ba0cec62fdc96c9fda`  
		Last Modified: Thu, 22 May 2025 02:54:55 GMT  
		Size: 200.2 MB (200220133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e283810be4e98386f3e32049fd4b37093f1e511e6080b1851c9256ec87cf016c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d9c85b832829e5a61565f5553a60b93dcfb37f6a329aaef650e215fb76f84d`

```dockerfile
```

-	Layers:
	-	`sha256:d0f3a891a4706bed94b5fc20f33060dff370905ed11bcf882d2c5a7c19a87236`  
		Last Modified: Thu, 22 May 2025 02:54:50 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:132fea97bf17a4e50202ebf282f29f0e798f269ffd2d03f5179dec066727f676
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
$ docker pull dart@sha256:2222e19c4919c213d31671d9520638bd2145a2309d830320345911677c088a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285788537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05343bcf107420ac814ade4895850bcfb53ada10cd2c9aa3d63c277312fc130`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7123238830b26d9d6f99d0a307a767f7e574ae279f3a5f5fcb59c83485ab33a0`  
		Last Modified: Wed, 21 May 2025 23:21:47 GMT  
		Size: 54.9 MB (54910399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97d53a7f96d3af27752768f441d35a380a4998932a993de3673dc02066a66db`  
		Last Modified: Wed, 21 May 2025 23:21:45 GMT  
		Size: 1.8 MB (1785450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f699c90a02cbcec5f1358e98ed290d3eb3c4800e5b101d3ade8040123a2ae138`  
		Last Modified: Wed, 21 May 2025 23:21:52 GMT  
		Size: 200.9 MB (200867326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:2116c2c5d77e64cb7d5752d5f671e0385c901740da309541171e4a5f9472f502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f51ff8a0c44b7e80fa66fd729a71b2386351eb569300f69f71f21e21a549d5`

```dockerfile
```

-	Layers:
	-	`sha256:3b701385ae480c2a18be93ead4c5700cc1bdbf922f8e2ade08a02dc5a5aab5fa`  
		Last Modified: Wed, 21 May 2025 23:21:45 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:8c841c0365614a7110ea1094a170a12ad2acd9e7d01c2099a0139c7ce3dfda81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214484649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c8ddb85e40e27b040e78006f693ea720db48a3489b72b8095a1ccd8f7615d8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c85147be7637b7c2750d42cfef2af5f2b7a9b21edf1baf341d3b9ff16d0d0b`  
		Last Modified: Thu, 22 May 2025 02:37:05 GMT  
		Size: 49.6 MB (49554662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40929bf8357109c1a8d00381005b544ba68df0322b49f6d2e58998e671ea0c84`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8228dade2aae6a866cc69c1ce0d31ec35ba591e688ac2be90cbd2caaa8748dab`  
		Last Modified: Thu, 22 May 2025 02:37:08 GMT  
		Size: 139.8 MB (139775089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:80cc4ce8a404af69cae44fb4fa602974c628991835b1f6a685d6a8e5752dec31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5359819d922d2bc9ecd3cebf3669da8fff341cd348816edfc386a79e3e73af27`

```dockerfile
```

-	Layers:
	-	`sha256:74cd3f041d7288142aa9523090c8d0347a88875125fca9485c9d1109018f92b2`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b04a1e339a9297a6aa4a42d29bba0840899f8d5da1127fe14f0ab2d4c401fc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284455973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac49d57b0bfd8415a228904cde303c9460c8f8542095854f753c4dfaf5f8a4a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cdc3e6a7951a95ca3a23969c311e0f260d2d126d6c9dff5126c9c2e83e4d94`  
		Last Modified: Thu, 22 May 2025 02:54:52 GMT  
		Size: 54.7 MB (54682308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65dae3b9ea3c5d4fbe78324186a1864aa7f37d2ed0ea7d3a97878375c5d86603`  
		Last Modified: Thu, 22 May 2025 02:54:50 GMT  
		Size: 1.5 MB (1488220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2422e8d91b945786bc4d4db6f0ef8e3f2bf7b25dd0eff0ba0cec62fdc96c9fda`  
		Last Modified: Thu, 22 May 2025 02:54:55 GMT  
		Size: 200.2 MB (200220133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:e283810be4e98386f3e32049fd4b37093f1e511e6080b1851c9256ec87cf016c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d9c85b832829e5a61565f5553a60b93dcfb37f6a329aaef650e215fb76f84d`

```dockerfile
```

-	Layers:
	-	`sha256:d0f3a891a4706bed94b5fc20f33060dff370905ed11bcf882d2c5a7c19a87236`  
		Last Modified: Thu, 22 May 2025 02:54:50 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:132fea97bf17a4e50202ebf282f29f0e798f269ffd2d03f5179dec066727f676
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
$ docker pull dart@sha256:2222e19c4919c213d31671d9520638bd2145a2309d830320345911677c088a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285788537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05343bcf107420ac814ade4895850bcfb53ada10cd2c9aa3d63c277312fc130`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7123238830b26d9d6f99d0a307a767f7e574ae279f3a5f5fcb59c83485ab33a0`  
		Last Modified: Wed, 21 May 2025 23:21:47 GMT  
		Size: 54.9 MB (54910399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97d53a7f96d3af27752768f441d35a380a4998932a993de3673dc02066a66db`  
		Last Modified: Wed, 21 May 2025 23:21:45 GMT  
		Size: 1.8 MB (1785450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f699c90a02cbcec5f1358e98ed290d3eb3c4800e5b101d3ade8040123a2ae138`  
		Last Modified: Wed, 21 May 2025 23:21:52 GMT  
		Size: 200.9 MB (200867326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:2116c2c5d77e64cb7d5752d5f671e0385c901740da309541171e4a5f9472f502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f51ff8a0c44b7e80fa66fd729a71b2386351eb569300f69f71f21e21a549d5`

```dockerfile
```

-	Layers:
	-	`sha256:3b701385ae480c2a18be93ead4c5700cc1bdbf922f8e2ade08a02dc5a5aab5fa`  
		Last Modified: Wed, 21 May 2025 23:21:45 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:8c841c0365614a7110ea1094a170a12ad2acd9e7d01c2099a0139c7ce3dfda81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214484649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c8ddb85e40e27b040e78006f693ea720db48a3489b72b8095a1ccd8f7615d8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c85147be7637b7c2750d42cfef2af5f2b7a9b21edf1baf341d3b9ff16d0d0b`  
		Last Modified: Thu, 22 May 2025 02:37:05 GMT  
		Size: 49.6 MB (49554662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40929bf8357109c1a8d00381005b544ba68df0322b49f6d2e58998e671ea0c84`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8228dade2aae6a866cc69c1ce0d31ec35ba591e688ac2be90cbd2caaa8748dab`  
		Last Modified: Thu, 22 May 2025 02:37:08 GMT  
		Size: 139.8 MB (139775089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:80cc4ce8a404af69cae44fb4fa602974c628991835b1f6a685d6a8e5752dec31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5359819d922d2bc9ecd3cebf3669da8fff341cd348816edfc386a79e3e73af27`

```dockerfile
```

-	Layers:
	-	`sha256:74cd3f041d7288142aa9523090c8d0347a88875125fca9485c9d1109018f92b2`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b04a1e339a9297a6aa4a42d29bba0840899f8d5da1127fe14f0ab2d4c401fc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284455973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac49d57b0bfd8415a228904cde303c9460c8f8542095854f753c4dfaf5f8a4a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=122eae1e412ffae9b2667470ec025e5811d064847da95b22341b78445868f3ce;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9a83fea7025762811432a62eb409554f1425c004f7cb24bba396097ee5b36488;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5e6ba94c6077b30dc9485841c70a4d8a6ffa34ea35ccd138b2c218089e9ff525;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cdc3e6a7951a95ca3a23969c311e0f260d2d126d6c9dff5126c9c2e83e4d94`  
		Last Modified: Thu, 22 May 2025 02:54:52 GMT  
		Size: 54.7 MB (54682308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65dae3b9ea3c5d4fbe78324186a1864aa7f37d2ed0ea7d3a97878375c5d86603`  
		Last Modified: Thu, 22 May 2025 02:54:50 GMT  
		Size: 1.5 MB (1488220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2422e8d91b945786bc4d4db6f0ef8e3f2bf7b25dd0eff0ba0cec62fdc96c9fda`  
		Last Modified: Thu, 22 May 2025 02:54:55 GMT  
		Size: 200.2 MB (200220133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e283810be4e98386f3e32049fd4b37093f1e511e6080b1851c9256ec87cf016c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d9c85b832829e5a61565f5553a60b93dcfb37f6a329aaef650e215fb76f84d`

```dockerfile
```

-	Layers:
	-	`sha256:d0f3a891a4706bed94b5fc20f33060dff370905ed11bcf882d2c5a7c19a87236`  
		Last Modified: Thu, 22 May 2025 02:54:50 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json
