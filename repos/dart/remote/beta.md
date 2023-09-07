## `dart:beta`

```console
$ docker pull dart@sha256:4633d387fb558ae16477a19e81c9444591142d5da879d903d137872f325fda81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:5fb698c392035ce722ac81fb5009ababeb5bb938cdbb3f6a28eb23cbe9d8b26d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.0 MB (303020110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118c228dbc71ba4684e54a4a9496262d50f00e1db0085f0fda03935be9698788`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 07:21:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 07:21:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 16 Aug 2023 07:21:32 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 18 Aug 2023 23:19:26 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Aug 2023 23:19:26 GMT
WORKDIR /root
# Fri, 01 Sep 2023 19:23:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bd0311f604def7e49215c6fbed823dc01284586f83963b6891cc6dee36da2488;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8bb319c661278852b371bd4438cc6e19860d0613bfe3d016006bd6ef6bf9e72f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=02de2c59d14fe4fcbcc6da756457be6966cd399bee507b2980d0e3c76fa4a2e3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-42.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2577ff5100d24131ef5c0b1d5abb88623898588a87bafbed311deab71d09ee`  
		Last Modified: Wed, 16 Aug 2023 07:22:28 GMT  
		Size: 45.1 MB (45101830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4d59ba3d1a7503ca685749da21497c47644df01b1409c1ce14a6d494fd9436`  
		Last Modified: Wed, 16 Aug 2023 07:22:22 GMT  
		Size: 2.2 MB (2160697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ac73fe6ce0b7ec108bfbb51e8f032f3eb90b016f93022f1bfb19dc02857872`  
		Last Modified: Fri, 01 Sep 2023 19:23:49 GMT  
		Size: 224.3 MB (224339905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:fcf845077c906fedcd75b1995af1ba31dce4111ab09489d559cad7a1f150f22c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185617173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a1286c0af1a438e95a59437d4fb21eb8626cece52f51a3ac63cf910ac59ee3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:58:09 GMT
ADD file:d714939aacc810de397a02461ce4b9dd85e92783aff066bd3da685e3d2d97439 in / 
# Thu, 07 Sep 2023 00:58:10 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:55:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:55:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 07 Sep 2023 01:55:59 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 07 Sep 2023 01:55:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 01:55:59 GMT
WORKDIR /root
# Thu, 07 Sep 2023 01:56:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bd0311f604def7e49215c6fbed823dc01284586f83963b6891cc6dee36da2488;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8bb319c661278852b371bd4438cc6e19860d0613bfe3d016006bd6ef6bf9e72f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=02de2c59d14fe4fcbcc6da756457be6966cd399bee507b2980d0e3c76fa4a2e3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-42.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:323242406c24248128abc25e113055d272350b4ac4ecd985dbabfb7061c48d49`  
		Last Modified: Thu, 07 Sep 2023 01:03:12 GMT  
		Size: 26.6 MB (26578710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aeaeabc9eed5e4b6207b4f729dc6c8f8acc154299578e082a7e1e6d570a18b6`  
		Last Modified: Thu, 07 Sep 2023 01:56:59 GMT  
		Size: 41.0 MB (40988287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf7fe56ae6697aba2588a366d664e58dc3243c87d2f1ac39d7b64fe1a6a7914`  
		Last Modified: Thu, 07 Sep 2023 01:56:49 GMT  
		Size: 1.3 MB (1287721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd8101581f7780a8836f10b874d020e992c6264689c51ce617143b27fe65703`  
		Last Modified: Thu, 07 Sep 2023 01:57:59 GMT  
		Size: 116.8 MB (116762455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:ea5b7d54d41eea1f1b17354217c4f1303882487ac1296520ca431a9e601cf6c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194789635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f859467c244af46671e9484df9da3c9577b42cb97c7138f7c20377d225f79c1e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 02:02:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 02:02:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 16 Aug 2023 02:02:18 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 18 Aug 2023 23:39:25 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Aug 2023 23:39:25 GMT
WORKDIR /root
# Fri, 01 Sep 2023 19:40:26 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bd0311f604def7e49215c6fbed823dc01284586f83963b6891cc6dee36da2488;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8bb319c661278852b371bd4438cc6e19860d0613bfe3d016006bd6ef6bf9e72f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=02de2c59d14fe4fcbcc6da756457be6966cd399bee507b2980d0e3c76fa4a2e3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-42.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c88ee4e2ded4b674611c7a0cc207fa18d0c207f6898b4c4a97598b60dc687d3`  
		Last Modified: Wed, 16 Aug 2023 02:03:00 GMT  
		Size: 45.0 MB (45011889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26f4393bc25a5d3316c200e692678aa19db82688e7b1d5442111eecc8273919`  
		Last Modified: Wed, 16 Aug 2023 02:02:55 GMT  
		Size: 1.6 MB (1560880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca2d1b7c7931a0f8b124e71f2500ff4fc00fc41b3e8c47f5b80e1b813b29d30`  
		Last Modified: Fri, 01 Sep 2023 19:40:54 GMT  
		Size: 118.2 MB (118154050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
