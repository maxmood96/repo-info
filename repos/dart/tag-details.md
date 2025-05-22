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
$ docker pull dart@sha256:945277de3e08fbd3ca804d33e7c3b5c3098922846849646f85187f0ce56a9277
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
$ docker pull dart@sha256:4c5e76adab70f56720b931d3ee5ede056a8c0aadd2ebe1eecb0703d8cf24b018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214489773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d8d784d2d7939bdc6eb3187e7546bebc2f1e32b65a391a644927be58a9c8c3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421616deef9a566da897ddca5ce757795bb3b2b25ac0d30eba9a17f08a426363`  
		Last Modified: Tue, 20 May 2025 21:29:12 GMT  
		Size: 49.6 MB (49554624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676269a37296c186c0d1fbfd9bb22c18ce548e1e1acfa1d43a7e66da0881625a`  
		Last Modified: Tue, 20 May 2025 21:29:10 GMT  
		Size: 1.2 MB (1221937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0636192845ad62486c289fc8211e2794a272f8f1f23d712391876e65a67d4356`  
		Last Modified: Tue, 20 May 2025 21:29:14 GMT  
		Size: 139.8 MB (139775106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:536d09637a4a74b224cda5c173d92f72a540053481f31a624a0ffa73e7a85780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12c2a8299e9f068338e33d8b0c00489bd5889e7f207f7820d40c54d1714959e`

```dockerfile
```

-	Layers:
	-	`sha256:e8e68d95fc01d291083f3b298d2d5484144b55b9238102a8a89fc3dbcf80e9e3`  
		Last Modified: Tue, 20 May 2025 21:29:10 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:17905fde115b2cb1f699acc9af9a8a2edc4c46909db000c7bc2b55e20564e323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284457660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0240de1dca312e4e560e41ffcc498fa0cc2d0c6bfac1d1c4f7c52a17dfe2a75d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee44402cd7e21214b48429542879b126e6935c784a5076c43750c0d5edf988d`  
		Last Modified: Tue, 20 May 2025 21:29:06 GMT  
		Size: 54.7 MB (54682705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33543c22a32c8caec2b404cebfb4e2d7f2e895394ee7fd4d5a3c607e1e3db417`  
		Last Modified: Tue, 20 May 2025 21:29:05 GMT  
		Size: 1.5 MB (1488214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903d202c1d5261a1f0127cb80600ec27d9d2114f7b48b7f019151e4a7beecedc`  
		Last Modified: Tue, 20 May 2025 21:29:11 GMT  
		Size: 200.2 MB (200220087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:755604503db1ec7745485364c7d1b7e04b6df2fb45719a3e782fa132e85730f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915a5214654ea51229617c4e4bf6fe4cafca6d2edf1695297313388ca17045fe`

```dockerfile
```

-	Layers:
	-	`sha256:f9300b0ebd0e64b7c18d031796765418d346bf9ff1739e123af0ee846c943a8b`  
		Last Modified: Tue, 20 May 2025 21:29:05 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:945277de3e08fbd3ca804d33e7c3b5c3098922846849646f85187f0ce56a9277
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
$ docker pull dart@sha256:4c5e76adab70f56720b931d3ee5ede056a8c0aadd2ebe1eecb0703d8cf24b018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214489773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d8d784d2d7939bdc6eb3187e7546bebc2f1e32b65a391a644927be58a9c8c3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421616deef9a566da897ddca5ce757795bb3b2b25ac0d30eba9a17f08a426363`  
		Last Modified: Tue, 20 May 2025 21:29:12 GMT  
		Size: 49.6 MB (49554624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676269a37296c186c0d1fbfd9bb22c18ce548e1e1acfa1d43a7e66da0881625a`  
		Last Modified: Tue, 20 May 2025 21:29:10 GMT  
		Size: 1.2 MB (1221937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0636192845ad62486c289fc8211e2794a272f8f1f23d712391876e65a67d4356`  
		Last Modified: Tue, 20 May 2025 21:29:14 GMT  
		Size: 139.8 MB (139775106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:536d09637a4a74b224cda5c173d92f72a540053481f31a624a0ffa73e7a85780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12c2a8299e9f068338e33d8b0c00489bd5889e7f207f7820d40c54d1714959e`

```dockerfile
```

-	Layers:
	-	`sha256:e8e68d95fc01d291083f3b298d2d5484144b55b9238102a8a89fc3dbcf80e9e3`  
		Last Modified: Tue, 20 May 2025 21:29:10 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:17905fde115b2cb1f699acc9af9a8a2edc4c46909db000c7bc2b55e20564e323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284457660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0240de1dca312e4e560e41ffcc498fa0cc2d0c6bfac1d1c4f7c52a17dfe2a75d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee44402cd7e21214b48429542879b126e6935c784a5076c43750c0d5edf988d`  
		Last Modified: Tue, 20 May 2025 21:29:06 GMT  
		Size: 54.7 MB (54682705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33543c22a32c8caec2b404cebfb4e2d7f2e895394ee7fd4d5a3c607e1e3db417`  
		Last Modified: Tue, 20 May 2025 21:29:05 GMT  
		Size: 1.5 MB (1488214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903d202c1d5261a1f0127cb80600ec27d9d2114f7b48b7f019151e4a7beecedc`  
		Last Modified: Tue, 20 May 2025 21:29:11 GMT  
		Size: 200.2 MB (200220087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:755604503db1ec7745485364c7d1b7e04b6df2fb45719a3e782fa132e85730f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915a5214654ea51229617c4e4bf6fe4cafca6d2edf1695297313388ca17045fe`

```dockerfile
```

-	Layers:
	-	`sha256:f9300b0ebd0e64b7c18d031796765418d346bf9ff1739e123af0ee846c943a8b`  
		Last Modified: Tue, 20 May 2025 21:29:05 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8`

```console
$ docker pull dart@sha256:945277de3e08fbd3ca804d33e7c3b5c3098922846849646f85187f0ce56a9277
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
$ docker pull dart@sha256:4c5e76adab70f56720b931d3ee5ede056a8c0aadd2ebe1eecb0703d8cf24b018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214489773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d8d784d2d7939bdc6eb3187e7546bebc2f1e32b65a391a644927be58a9c8c3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421616deef9a566da897ddca5ce757795bb3b2b25ac0d30eba9a17f08a426363`  
		Last Modified: Tue, 20 May 2025 21:29:12 GMT  
		Size: 49.6 MB (49554624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676269a37296c186c0d1fbfd9bb22c18ce548e1e1acfa1d43a7e66da0881625a`  
		Last Modified: Tue, 20 May 2025 21:29:10 GMT  
		Size: 1.2 MB (1221937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0636192845ad62486c289fc8211e2794a272f8f1f23d712391876e65a67d4356`  
		Last Modified: Tue, 20 May 2025 21:29:14 GMT  
		Size: 139.8 MB (139775106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8` - unknown; unknown

```console
$ docker pull dart@sha256:536d09637a4a74b224cda5c173d92f72a540053481f31a624a0ffa73e7a85780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12c2a8299e9f068338e33d8b0c00489bd5889e7f207f7820d40c54d1714959e`

```dockerfile
```

-	Layers:
	-	`sha256:e8e68d95fc01d291083f3b298d2d5484144b55b9238102a8a89fc3dbcf80e9e3`  
		Last Modified: Tue, 20 May 2025 21:29:10 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:17905fde115b2cb1f699acc9af9a8a2edc4c46909db000c7bc2b55e20564e323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284457660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0240de1dca312e4e560e41ffcc498fa0cc2d0c6bfac1d1c4f7c52a17dfe2a75d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee44402cd7e21214b48429542879b126e6935c784a5076c43750c0d5edf988d`  
		Last Modified: Tue, 20 May 2025 21:29:06 GMT  
		Size: 54.7 MB (54682705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33543c22a32c8caec2b404cebfb4e2d7f2e895394ee7fd4d5a3c607e1e3db417`  
		Last Modified: Tue, 20 May 2025 21:29:05 GMT  
		Size: 1.5 MB (1488214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903d202c1d5261a1f0127cb80600ec27d9d2114f7b48b7f019151e4a7beecedc`  
		Last Modified: Tue, 20 May 2025 21:29:11 GMT  
		Size: 200.2 MB (200220087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8` - unknown; unknown

```console
$ docker pull dart@sha256:755604503db1ec7745485364c7d1b7e04b6df2fb45719a3e782fa132e85730f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915a5214654ea51229617c4e4bf6fe4cafca6d2edf1695297313388ca17045fe`

```dockerfile
```

-	Layers:
	-	`sha256:f9300b0ebd0e64b7c18d031796765418d346bf9ff1739e123af0ee846c943a8b`  
		Last Modified: Tue, 20 May 2025 21:29:05 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8-sdk`

```console
$ docker pull dart@sha256:945277de3e08fbd3ca804d33e7c3b5c3098922846849646f85187f0ce56a9277
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
$ docker pull dart@sha256:4c5e76adab70f56720b931d3ee5ede056a8c0aadd2ebe1eecb0703d8cf24b018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214489773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d8d784d2d7939bdc6eb3187e7546bebc2f1e32b65a391a644927be58a9c8c3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421616deef9a566da897ddca5ce757795bb3b2b25ac0d30eba9a17f08a426363`  
		Last Modified: Tue, 20 May 2025 21:29:12 GMT  
		Size: 49.6 MB (49554624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676269a37296c186c0d1fbfd9bb22c18ce548e1e1acfa1d43a7e66da0881625a`  
		Last Modified: Tue, 20 May 2025 21:29:10 GMT  
		Size: 1.2 MB (1221937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0636192845ad62486c289fc8211e2794a272f8f1f23d712391876e65a67d4356`  
		Last Modified: Tue, 20 May 2025 21:29:14 GMT  
		Size: 139.8 MB (139775106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:536d09637a4a74b224cda5c173d92f72a540053481f31a624a0ffa73e7a85780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12c2a8299e9f068338e33d8b0c00489bd5889e7f207f7820d40c54d1714959e`

```dockerfile
```

-	Layers:
	-	`sha256:e8e68d95fc01d291083f3b298d2d5484144b55b9238102a8a89fc3dbcf80e9e3`  
		Last Modified: Tue, 20 May 2025 21:29:10 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:17905fde115b2cb1f699acc9af9a8a2edc4c46909db000c7bc2b55e20564e323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284457660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0240de1dca312e4e560e41ffcc498fa0cc2d0c6bfac1d1c4f7c52a17dfe2a75d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee44402cd7e21214b48429542879b126e6935c784a5076c43750c0d5edf988d`  
		Last Modified: Tue, 20 May 2025 21:29:06 GMT  
		Size: 54.7 MB (54682705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33543c22a32c8caec2b404cebfb4e2d7f2e895394ee7fd4d5a3c607e1e3db417`  
		Last Modified: Tue, 20 May 2025 21:29:05 GMT  
		Size: 1.5 MB (1488214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903d202c1d5261a1f0127cb80600ec27d9d2114f7b48b7f019151e4a7beecedc`  
		Last Modified: Tue, 20 May 2025 21:29:11 GMT  
		Size: 200.2 MB (200220087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:755604503db1ec7745485364c7d1b7e04b6df2fb45719a3e782fa132e85730f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915a5214654ea51229617c4e4bf6fe4cafca6d2edf1695297313388ca17045fe`

```dockerfile
```

-	Layers:
	-	`sha256:f9300b0ebd0e64b7c18d031796765418d346bf9ff1739e123af0ee846c943a8b`  
		Last Modified: Tue, 20 May 2025 21:29:05 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8.0`

```console
$ docker pull dart@sha256:945277de3e08fbd3ca804d33e7c3b5c3098922846849646f85187f0ce56a9277
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
$ docker pull dart@sha256:4c5e76adab70f56720b931d3ee5ede056a8c0aadd2ebe1eecb0703d8cf24b018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214489773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d8d784d2d7939bdc6eb3187e7546bebc2f1e32b65a391a644927be58a9c8c3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421616deef9a566da897ddca5ce757795bb3b2b25ac0d30eba9a17f08a426363`  
		Last Modified: Tue, 20 May 2025 21:29:12 GMT  
		Size: 49.6 MB (49554624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676269a37296c186c0d1fbfd9bb22c18ce548e1e1acfa1d43a7e66da0881625a`  
		Last Modified: Tue, 20 May 2025 21:29:10 GMT  
		Size: 1.2 MB (1221937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0636192845ad62486c289fc8211e2794a272f8f1f23d712391876e65a67d4356`  
		Last Modified: Tue, 20 May 2025 21:29:14 GMT  
		Size: 139.8 MB (139775106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0` - unknown; unknown

```console
$ docker pull dart@sha256:536d09637a4a74b224cda5c173d92f72a540053481f31a624a0ffa73e7a85780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12c2a8299e9f068338e33d8b0c00489bd5889e7f207f7820d40c54d1714959e`

```dockerfile
```

-	Layers:
	-	`sha256:e8e68d95fc01d291083f3b298d2d5484144b55b9238102a8a89fc3dbcf80e9e3`  
		Last Modified: Tue, 20 May 2025 21:29:10 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.0` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:17905fde115b2cb1f699acc9af9a8a2edc4c46909db000c7bc2b55e20564e323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284457660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0240de1dca312e4e560e41ffcc498fa0cc2d0c6bfac1d1c4f7c52a17dfe2a75d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee44402cd7e21214b48429542879b126e6935c784a5076c43750c0d5edf988d`  
		Last Modified: Tue, 20 May 2025 21:29:06 GMT  
		Size: 54.7 MB (54682705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33543c22a32c8caec2b404cebfb4e2d7f2e895394ee7fd4d5a3c607e1e3db417`  
		Last Modified: Tue, 20 May 2025 21:29:05 GMT  
		Size: 1.5 MB (1488214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903d202c1d5261a1f0127cb80600ec27d9d2114f7b48b7f019151e4a7beecedc`  
		Last Modified: Tue, 20 May 2025 21:29:11 GMT  
		Size: 200.2 MB (200220087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0` - unknown; unknown

```console
$ docker pull dart@sha256:755604503db1ec7745485364c7d1b7e04b6df2fb45719a3e782fa132e85730f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915a5214654ea51229617c4e4bf6fe4cafca6d2edf1695297313388ca17045fe`

```dockerfile
```

-	Layers:
	-	`sha256:f9300b0ebd0e64b7c18d031796765418d346bf9ff1739e123af0ee846c943a8b`  
		Last Modified: Tue, 20 May 2025 21:29:05 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8.0-sdk`

```console
$ docker pull dart@sha256:945277de3e08fbd3ca804d33e7c3b5c3098922846849646f85187f0ce56a9277
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
$ docker pull dart@sha256:4c5e76adab70f56720b931d3ee5ede056a8c0aadd2ebe1eecb0703d8cf24b018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214489773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d8d784d2d7939bdc6eb3187e7546bebc2f1e32b65a391a644927be58a9c8c3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421616deef9a566da897ddca5ce757795bb3b2b25ac0d30eba9a17f08a426363`  
		Last Modified: Tue, 20 May 2025 21:29:12 GMT  
		Size: 49.6 MB (49554624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676269a37296c186c0d1fbfd9bb22c18ce548e1e1acfa1d43a7e66da0881625a`  
		Last Modified: Tue, 20 May 2025 21:29:10 GMT  
		Size: 1.2 MB (1221937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0636192845ad62486c289fc8211e2794a272f8f1f23d712391876e65a67d4356`  
		Last Modified: Tue, 20 May 2025 21:29:14 GMT  
		Size: 139.8 MB (139775106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:536d09637a4a74b224cda5c173d92f72a540053481f31a624a0ffa73e7a85780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12c2a8299e9f068338e33d8b0c00489bd5889e7f207f7820d40c54d1714959e`

```dockerfile
```

-	Layers:
	-	`sha256:e8e68d95fc01d291083f3b298d2d5484144b55b9238102a8a89fc3dbcf80e9e3`  
		Last Modified: Tue, 20 May 2025 21:29:10 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.0-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:17905fde115b2cb1f699acc9af9a8a2edc4c46909db000c7bc2b55e20564e323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284457660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0240de1dca312e4e560e41ffcc498fa0cc2d0c6bfac1d1c4f7c52a17dfe2a75d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee44402cd7e21214b48429542879b126e6935c784a5076c43750c0d5edf988d`  
		Last Modified: Tue, 20 May 2025 21:29:06 GMT  
		Size: 54.7 MB (54682705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33543c22a32c8caec2b404cebfb4e2d7f2e895394ee7fd4d5a3c607e1e3db417`  
		Last Modified: Tue, 20 May 2025 21:29:05 GMT  
		Size: 1.5 MB (1488214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903d202c1d5261a1f0127cb80600ec27d9d2114f7b48b7f019151e4a7beecedc`  
		Last Modified: Tue, 20 May 2025 21:29:11 GMT  
		Size: 200.2 MB (200220087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:755604503db1ec7745485364c7d1b7e04b6df2fb45719a3e782fa132e85730f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915a5214654ea51229617c4e4bf6fe4cafca6d2edf1695297313388ca17045fe`

```dockerfile
```

-	Layers:
	-	`sha256:f9300b0ebd0e64b7c18d031796765418d346bf9ff1739e123af0ee846c943a8b`  
		Last Modified: Tue, 20 May 2025 21:29:05 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9.0-100.2.beta`

```console
$ docker pull dart@sha256:7c5e57d33764d0e33e8e1db665c6f9b4d92357baeca59b3f5b90080fdc03250d
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
$ docker pull dart@sha256:d5ebe353b1cd02c03636fd6a093e7d9049af04d7cf29cef2e3b84695cdd9a0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223856156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ded9aa2e3ab72820da877dc333ae1c9cf28a5ff5e3059a00c82a1e564548488`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421616deef9a566da897ddca5ce757795bb3b2b25ac0d30eba9a17f08a426363`  
		Last Modified: Tue, 20 May 2025 21:29:12 GMT  
		Size: 49.6 MB (49554624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676269a37296c186c0d1fbfd9bb22c18ce548e1e1acfa1d43a7e66da0881625a`  
		Last Modified: Tue, 20 May 2025 21:29:10 GMT  
		Size: 1.2 MB (1221937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2dd100b1e20db1e45de3762a5da1aeb5b6268579bc39ecb0b4706211ebf5be`  
		Last Modified: Tue, 20 May 2025 21:30:05 GMT  
		Size: 149.1 MB (149141489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-100.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:76e2234166bbef2a67453e18e1fe6fa191f6510a4c6a030150ad2dd662cc8579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319a842e450b6d622ea4895c009fe949a598368ee1b91b10c2276c321a507286`

```dockerfile
```

-	Layers:
	-	`sha256:8b42d54b6e9b1100c95fddb098f9ff42f47c1d00880036b32da103f40b2983f3`  
		Last Modified: Tue, 20 May 2025 21:30:00 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.0-100.2.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:02e378d52177628546fff8561fee245319b79ecaa804f2d742527985afdc56d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298385759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a97ecc9db60edffcd665f793336d4caf185b23fb74c76b1b92c22962b98c77`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee44402cd7e21214b48429542879b126e6935c784a5076c43750c0d5edf988d`  
		Last Modified: Tue, 20 May 2025 21:29:06 GMT  
		Size: 54.7 MB (54682705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33543c22a32c8caec2b404cebfb4e2d7f2e895394ee7fd4d5a3c607e1e3db417`  
		Last Modified: Tue, 20 May 2025 21:29:05 GMT  
		Size: 1.5 MB (1488214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41477dbaa9ac7ac48bc22812a383c1862616eb7131e1b5302b9a3dd7d6cf5bd7`  
		Last Modified: Tue, 20 May 2025 21:30:00 GMT  
		Size: 214.1 MB (214148186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-100.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:5d55580f6de8555f3343faead2441936d0e75d62748691f9c2e7ad4d9318eb84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee8f5fe4d29da8af75785fd1d6b6421ba7afc400a0342bffacebbb925e61e37`

```dockerfile
```

-	Layers:
	-	`sha256:e9461176eb52e40d6f5fa8a5c059de3b72b82654db198f095c605536b22d3beb`  
		Last Modified: Tue, 20 May 2025 21:29:55 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9.0-100.2.beta-sdk`

```console
$ docker pull dart@sha256:7c5e57d33764d0e33e8e1db665c6f9b4d92357baeca59b3f5b90080fdc03250d
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
$ docker pull dart@sha256:d5ebe353b1cd02c03636fd6a093e7d9049af04d7cf29cef2e3b84695cdd9a0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223856156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ded9aa2e3ab72820da877dc333ae1c9cf28a5ff5e3059a00c82a1e564548488`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421616deef9a566da897ddca5ce757795bb3b2b25ac0d30eba9a17f08a426363`  
		Last Modified: Tue, 20 May 2025 21:29:12 GMT  
		Size: 49.6 MB (49554624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676269a37296c186c0d1fbfd9bb22c18ce548e1e1acfa1d43a7e66da0881625a`  
		Last Modified: Tue, 20 May 2025 21:29:10 GMT  
		Size: 1.2 MB (1221937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2dd100b1e20db1e45de3762a5da1aeb5b6268579bc39ecb0b4706211ebf5be`  
		Last Modified: Tue, 20 May 2025 21:30:05 GMT  
		Size: 149.1 MB (149141489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-100.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:76e2234166bbef2a67453e18e1fe6fa191f6510a4c6a030150ad2dd662cc8579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319a842e450b6d622ea4895c009fe949a598368ee1b91b10c2276c321a507286`

```dockerfile
```

-	Layers:
	-	`sha256:8b42d54b6e9b1100c95fddb098f9ff42f47c1d00880036b32da103f40b2983f3`  
		Last Modified: Tue, 20 May 2025 21:30:00 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.0-100.2.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:02e378d52177628546fff8561fee245319b79ecaa804f2d742527985afdc56d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298385759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a97ecc9db60edffcd665f793336d4caf185b23fb74c76b1b92c22962b98c77`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee44402cd7e21214b48429542879b126e6935c784a5076c43750c0d5edf988d`  
		Last Modified: Tue, 20 May 2025 21:29:06 GMT  
		Size: 54.7 MB (54682705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33543c22a32c8caec2b404cebfb4e2d7f2e895394ee7fd4d5a3c607e1e3db417`  
		Last Modified: Tue, 20 May 2025 21:29:05 GMT  
		Size: 1.5 MB (1488214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41477dbaa9ac7ac48bc22812a383c1862616eb7131e1b5302b9a3dd7d6cf5bd7`  
		Last Modified: Tue, 20 May 2025 21:30:00 GMT  
		Size: 214.1 MB (214148186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-100.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5d55580f6de8555f3343faead2441936d0e75d62748691f9c2e7ad4d9318eb84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee8f5fe4d29da8af75785fd1d6b6421ba7afc400a0342bffacebbb925e61e37`

```dockerfile
```

-	Layers:
	-	`sha256:e9461176eb52e40d6f5fa8a5c059de3b72b82654db198f095c605536b22d3beb`  
		Last Modified: Tue, 20 May 2025 21:29:55 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:7c5e57d33764d0e33e8e1db665c6f9b4d92357baeca59b3f5b90080fdc03250d
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
$ docker pull dart@sha256:d5ebe353b1cd02c03636fd6a093e7d9049af04d7cf29cef2e3b84695cdd9a0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223856156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ded9aa2e3ab72820da877dc333ae1c9cf28a5ff5e3059a00c82a1e564548488`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421616deef9a566da897ddca5ce757795bb3b2b25ac0d30eba9a17f08a426363`  
		Last Modified: Tue, 20 May 2025 21:29:12 GMT  
		Size: 49.6 MB (49554624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676269a37296c186c0d1fbfd9bb22c18ce548e1e1acfa1d43a7e66da0881625a`  
		Last Modified: Tue, 20 May 2025 21:29:10 GMT  
		Size: 1.2 MB (1221937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2dd100b1e20db1e45de3762a5da1aeb5b6268579bc39ecb0b4706211ebf5be`  
		Last Modified: Tue, 20 May 2025 21:30:05 GMT  
		Size: 149.1 MB (149141489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:76e2234166bbef2a67453e18e1fe6fa191f6510a4c6a030150ad2dd662cc8579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319a842e450b6d622ea4895c009fe949a598368ee1b91b10c2276c321a507286`

```dockerfile
```

-	Layers:
	-	`sha256:8b42d54b6e9b1100c95fddb098f9ff42f47c1d00880036b32da103f40b2983f3`  
		Last Modified: Tue, 20 May 2025 21:30:00 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:02e378d52177628546fff8561fee245319b79ecaa804f2d742527985afdc56d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298385759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a97ecc9db60edffcd665f793336d4caf185b23fb74c76b1b92c22962b98c77`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee44402cd7e21214b48429542879b126e6935c784a5076c43750c0d5edf988d`  
		Last Modified: Tue, 20 May 2025 21:29:06 GMT  
		Size: 54.7 MB (54682705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33543c22a32c8caec2b404cebfb4e2d7f2e895394ee7fd4d5a3c607e1e3db417`  
		Last Modified: Tue, 20 May 2025 21:29:05 GMT  
		Size: 1.5 MB (1488214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41477dbaa9ac7ac48bc22812a383c1862616eb7131e1b5302b9a3dd7d6cf5bd7`  
		Last Modified: Tue, 20 May 2025 21:30:00 GMT  
		Size: 214.1 MB (214148186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:5d55580f6de8555f3343faead2441936d0e75d62748691f9c2e7ad4d9318eb84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee8f5fe4d29da8af75785fd1d6b6421ba7afc400a0342bffacebbb925e61e37`

```dockerfile
```

-	Layers:
	-	`sha256:e9461176eb52e40d6f5fa8a5c059de3b72b82654db198f095c605536b22d3beb`  
		Last Modified: Tue, 20 May 2025 21:29:55 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:7c5e57d33764d0e33e8e1db665c6f9b4d92357baeca59b3f5b90080fdc03250d
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
$ docker pull dart@sha256:d5ebe353b1cd02c03636fd6a093e7d9049af04d7cf29cef2e3b84695cdd9a0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223856156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ded9aa2e3ab72820da877dc333ae1c9cf28a5ff5e3059a00c82a1e564548488`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421616deef9a566da897ddca5ce757795bb3b2b25ac0d30eba9a17f08a426363`  
		Last Modified: Tue, 20 May 2025 21:29:12 GMT  
		Size: 49.6 MB (49554624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676269a37296c186c0d1fbfd9bb22c18ce548e1e1acfa1d43a7e66da0881625a`  
		Last Modified: Tue, 20 May 2025 21:29:10 GMT  
		Size: 1.2 MB (1221937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2dd100b1e20db1e45de3762a5da1aeb5b6268579bc39ecb0b4706211ebf5be`  
		Last Modified: Tue, 20 May 2025 21:30:05 GMT  
		Size: 149.1 MB (149141489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:76e2234166bbef2a67453e18e1fe6fa191f6510a4c6a030150ad2dd662cc8579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319a842e450b6d622ea4895c009fe949a598368ee1b91b10c2276c321a507286`

```dockerfile
```

-	Layers:
	-	`sha256:8b42d54b6e9b1100c95fddb098f9ff42f47c1d00880036b32da103f40b2983f3`  
		Last Modified: Tue, 20 May 2025 21:30:00 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:02e378d52177628546fff8561fee245319b79ecaa804f2d742527985afdc56d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298385759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a97ecc9db60edffcd665f793336d4caf185b23fb74c76b1b92c22962b98c77`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee44402cd7e21214b48429542879b126e6935c784a5076c43750c0d5edf988d`  
		Last Modified: Tue, 20 May 2025 21:29:06 GMT  
		Size: 54.7 MB (54682705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33543c22a32c8caec2b404cebfb4e2d7f2e895394ee7fd4d5a3c607e1e3db417`  
		Last Modified: Tue, 20 May 2025 21:29:05 GMT  
		Size: 1.5 MB (1488214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41477dbaa9ac7ac48bc22812a383c1862616eb7131e1b5302b9a3dd7d6cf5bd7`  
		Last Modified: Tue, 20 May 2025 21:30:00 GMT  
		Size: 214.1 MB (214148186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5d55580f6de8555f3343faead2441936d0e75d62748691f9c2e7ad4d9318eb84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee8f5fe4d29da8af75785fd1d6b6421ba7afc400a0342bffacebbb925e61e37`

```dockerfile
```

-	Layers:
	-	`sha256:e9461176eb52e40d6f5fa8a5c059de3b72b82654db198f095c605536b22d3beb`  
		Last Modified: Tue, 20 May 2025 21:29:55 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:945277de3e08fbd3ca804d33e7c3b5c3098922846849646f85187f0ce56a9277
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
$ docker pull dart@sha256:4c5e76adab70f56720b931d3ee5ede056a8c0aadd2ebe1eecb0703d8cf24b018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214489773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d8d784d2d7939bdc6eb3187e7546bebc2f1e32b65a391a644927be58a9c8c3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421616deef9a566da897ddca5ce757795bb3b2b25ac0d30eba9a17f08a426363`  
		Last Modified: Tue, 20 May 2025 21:29:12 GMT  
		Size: 49.6 MB (49554624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676269a37296c186c0d1fbfd9bb22c18ce548e1e1acfa1d43a7e66da0881625a`  
		Last Modified: Tue, 20 May 2025 21:29:10 GMT  
		Size: 1.2 MB (1221937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0636192845ad62486c289fc8211e2794a272f8f1f23d712391876e65a67d4356`  
		Last Modified: Tue, 20 May 2025 21:29:14 GMT  
		Size: 139.8 MB (139775106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:536d09637a4a74b224cda5c173d92f72a540053481f31a624a0ffa73e7a85780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12c2a8299e9f068338e33d8b0c00489bd5889e7f207f7820d40c54d1714959e`

```dockerfile
```

-	Layers:
	-	`sha256:e8e68d95fc01d291083f3b298d2d5484144b55b9238102a8a89fc3dbcf80e9e3`  
		Last Modified: Tue, 20 May 2025 21:29:10 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:17905fde115b2cb1f699acc9af9a8a2edc4c46909db000c7bc2b55e20564e323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284457660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0240de1dca312e4e560e41ffcc498fa0cc2d0c6bfac1d1c4f7c52a17dfe2a75d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee44402cd7e21214b48429542879b126e6935c784a5076c43750c0d5edf988d`  
		Last Modified: Tue, 20 May 2025 21:29:06 GMT  
		Size: 54.7 MB (54682705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33543c22a32c8caec2b404cebfb4e2d7f2e895394ee7fd4d5a3c607e1e3db417`  
		Last Modified: Tue, 20 May 2025 21:29:05 GMT  
		Size: 1.5 MB (1488214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903d202c1d5261a1f0127cb80600ec27d9d2114f7b48b7f019151e4a7beecedc`  
		Last Modified: Tue, 20 May 2025 21:29:11 GMT  
		Size: 200.2 MB (200220087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:755604503db1ec7745485364c7d1b7e04b6df2fb45719a3e782fa132e85730f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915a5214654ea51229617c4e4bf6fe4cafca6d2edf1695297313388ca17045fe`

```dockerfile
```

-	Layers:
	-	`sha256:f9300b0ebd0e64b7c18d031796765418d346bf9ff1739e123af0ee846c943a8b`  
		Last Modified: Tue, 20 May 2025 21:29:05 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:945277de3e08fbd3ca804d33e7c3b5c3098922846849646f85187f0ce56a9277
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
$ docker pull dart@sha256:4c5e76adab70f56720b931d3ee5ede056a8c0aadd2ebe1eecb0703d8cf24b018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214489773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d8d784d2d7939bdc6eb3187e7546bebc2f1e32b65a391a644927be58a9c8c3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421616deef9a566da897ddca5ce757795bb3b2b25ac0d30eba9a17f08a426363`  
		Last Modified: Tue, 20 May 2025 21:29:12 GMT  
		Size: 49.6 MB (49554624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676269a37296c186c0d1fbfd9bb22c18ce548e1e1acfa1d43a7e66da0881625a`  
		Last Modified: Tue, 20 May 2025 21:29:10 GMT  
		Size: 1.2 MB (1221937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0636192845ad62486c289fc8211e2794a272f8f1f23d712391876e65a67d4356`  
		Last Modified: Tue, 20 May 2025 21:29:14 GMT  
		Size: 139.8 MB (139775106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:536d09637a4a74b224cda5c173d92f72a540053481f31a624a0ffa73e7a85780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12c2a8299e9f068338e33d8b0c00489bd5889e7f207f7820d40c54d1714959e`

```dockerfile
```

-	Layers:
	-	`sha256:e8e68d95fc01d291083f3b298d2d5484144b55b9238102a8a89fc3dbcf80e9e3`  
		Last Modified: Tue, 20 May 2025 21:29:10 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:17905fde115b2cb1f699acc9af9a8a2edc4c46909db000c7bc2b55e20564e323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284457660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0240de1dca312e4e560e41ffcc498fa0cc2d0c6bfac1d1c4f7c52a17dfe2a75d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee44402cd7e21214b48429542879b126e6935c784a5076c43750c0d5edf988d`  
		Last Modified: Tue, 20 May 2025 21:29:06 GMT  
		Size: 54.7 MB (54682705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33543c22a32c8caec2b404cebfb4e2d7f2e895394ee7fd4d5a3c607e1e3db417`  
		Last Modified: Tue, 20 May 2025 21:29:05 GMT  
		Size: 1.5 MB (1488214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903d202c1d5261a1f0127cb80600ec27d9d2114f7b48b7f019151e4a7beecedc`  
		Last Modified: Tue, 20 May 2025 21:29:11 GMT  
		Size: 200.2 MB (200220087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:755604503db1ec7745485364c7d1b7e04b6df2fb45719a3e782fa132e85730f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915a5214654ea51229617c4e4bf6fe4cafca6d2edf1695297313388ca17045fe`

```dockerfile
```

-	Layers:
	-	`sha256:f9300b0ebd0e64b7c18d031796765418d346bf9ff1739e123af0ee846c943a8b`  
		Last Modified: Tue, 20 May 2025 21:29:05 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:945277de3e08fbd3ca804d33e7c3b5c3098922846849646f85187f0ce56a9277
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
$ docker pull dart@sha256:4c5e76adab70f56720b931d3ee5ede056a8c0aadd2ebe1eecb0703d8cf24b018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214489773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d8d784d2d7939bdc6eb3187e7546bebc2f1e32b65a391a644927be58a9c8c3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421616deef9a566da897ddca5ce757795bb3b2b25ac0d30eba9a17f08a426363`  
		Last Modified: Tue, 20 May 2025 21:29:12 GMT  
		Size: 49.6 MB (49554624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676269a37296c186c0d1fbfd9bb22c18ce548e1e1acfa1d43a7e66da0881625a`  
		Last Modified: Tue, 20 May 2025 21:29:10 GMT  
		Size: 1.2 MB (1221937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0636192845ad62486c289fc8211e2794a272f8f1f23d712391876e65a67d4356`  
		Last Modified: Tue, 20 May 2025 21:29:14 GMT  
		Size: 139.8 MB (139775106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:536d09637a4a74b224cda5c173d92f72a540053481f31a624a0ffa73e7a85780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12c2a8299e9f068338e33d8b0c00489bd5889e7f207f7820d40c54d1714959e`

```dockerfile
```

-	Layers:
	-	`sha256:e8e68d95fc01d291083f3b298d2d5484144b55b9238102a8a89fc3dbcf80e9e3`  
		Last Modified: Tue, 20 May 2025 21:29:10 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:17905fde115b2cb1f699acc9af9a8a2edc4c46909db000c7bc2b55e20564e323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284457660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0240de1dca312e4e560e41ffcc498fa0cc2d0c6bfac1d1c4f7c52a17dfe2a75d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee44402cd7e21214b48429542879b126e6935c784a5076c43750c0d5edf988d`  
		Last Modified: Tue, 20 May 2025 21:29:06 GMT  
		Size: 54.7 MB (54682705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33543c22a32c8caec2b404cebfb4e2d7f2e895394ee7fd4d5a3c607e1e3db417`  
		Last Modified: Tue, 20 May 2025 21:29:05 GMT  
		Size: 1.5 MB (1488214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903d202c1d5261a1f0127cb80600ec27d9d2114f7b48b7f019151e4a7beecedc`  
		Last Modified: Tue, 20 May 2025 21:29:11 GMT  
		Size: 200.2 MB (200220087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:755604503db1ec7745485364c7d1b7e04b6df2fb45719a3e782fa132e85730f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915a5214654ea51229617c4e4bf6fe4cafca6d2edf1695297313388ca17045fe`

```dockerfile
```

-	Layers:
	-	`sha256:f9300b0ebd0e64b7c18d031796765418d346bf9ff1739e123af0ee846c943a8b`  
		Last Modified: Tue, 20 May 2025 21:29:05 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:945277de3e08fbd3ca804d33e7c3b5c3098922846849646f85187f0ce56a9277
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
$ docker pull dart@sha256:4c5e76adab70f56720b931d3ee5ede056a8c0aadd2ebe1eecb0703d8cf24b018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214489773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d8d784d2d7939bdc6eb3187e7546bebc2f1e32b65a391a644927be58a9c8c3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421616deef9a566da897ddca5ce757795bb3b2b25ac0d30eba9a17f08a426363`  
		Last Modified: Tue, 20 May 2025 21:29:12 GMT  
		Size: 49.6 MB (49554624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676269a37296c186c0d1fbfd9bb22c18ce548e1e1acfa1d43a7e66da0881625a`  
		Last Modified: Tue, 20 May 2025 21:29:10 GMT  
		Size: 1.2 MB (1221937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0636192845ad62486c289fc8211e2794a272f8f1f23d712391876e65a67d4356`  
		Last Modified: Tue, 20 May 2025 21:29:14 GMT  
		Size: 139.8 MB (139775106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:536d09637a4a74b224cda5c173d92f72a540053481f31a624a0ffa73e7a85780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12c2a8299e9f068338e33d8b0c00489bd5889e7f207f7820d40c54d1714959e`

```dockerfile
```

-	Layers:
	-	`sha256:e8e68d95fc01d291083f3b298d2d5484144b55b9238102a8a89fc3dbcf80e9e3`  
		Last Modified: Tue, 20 May 2025 21:29:10 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:17905fde115b2cb1f699acc9af9a8a2edc4c46909db000c7bc2b55e20564e323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284457660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0240de1dca312e4e560e41ffcc498fa0cc2d0c6bfac1d1c4f7c52a17dfe2a75d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee44402cd7e21214b48429542879b126e6935c784a5076c43750c0d5edf988d`  
		Last Modified: Tue, 20 May 2025 21:29:06 GMT  
		Size: 54.7 MB (54682705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33543c22a32c8caec2b404cebfb4e2d7f2e895394ee7fd4d5a3c607e1e3db417`  
		Last Modified: Tue, 20 May 2025 21:29:05 GMT  
		Size: 1.5 MB (1488214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903d202c1d5261a1f0127cb80600ec27d9d2114f7b48b7f019151e4a7beecedc`  
		Last Modified: Tue, 20 May 2025 21:29:11 GMT  
		Size: 200.2 MB (200220087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:755604503db1ec7745485364c7d1b7e04b6df2fb45719a3e782fa132e85730f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915a5214654ea51229617c4e4bf6fe4cafca6d2edf1695297313388ca17045fe`

```dockerfile
```

-	Layers:
	-	`sha256:f9300b0ebd0e64b7c18d031796765418d346bf9ff1739e123af0ee846c943a8b`  
		Last Modified: Tue, 20 May 2025 21:29:05 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json
