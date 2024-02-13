## `dart:sdk`

```console
$ docker pull dart@sha256:a40513b89e61d043fca9f8d76d4e95e9a3a84031041620a616f7e8702600084e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:fee670e4e6bf38c0e31d1ce0fce65539131c90407df83c5275c07c6cfe6d7193
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.5 MB (308534485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f045bdaa190b6cf34186a1f07bda5756c5cadf768aa775a76f2a029297a05d96`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:39:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:39:19 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Feb 2024 01:39:19 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Feb 2024 01:39:19 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 01:39:19 GMT
WORKDIR /root
# Tue, 13 Feb 2024 01:39:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=253390a14f6f5d764c82df4b2c2cf18a1c30a8e1fe0849448cc4fedabaaf1d48;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ee647813284e4464a46ffcf9af36ef8d891494056238f7b52a0485fcdefedb5a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9818a37dd39e8e91a0159bdd2522213f9d36bbd99b715465b4606190e6ae41c3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf37a55445764820f054ae98273dde04af1363504263e256cbd7fdabc62e2e3`  
		Last Modified: Tue, 13 Feb 2024 01:40:19 GMT  
		Size: 54.7 MB (54651436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961eb420cb87447b4a70c0d48b1e04cea2e6ab2ae6c029f97fb0d20190a1dfd0`  
		Last Modified: Tue, 13 Feb 2024 01:40:12 GMT  
		Size: 1.8 MB (1800726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3689c7af9f235a5cd1cfa13598ee6796e91b336ee80a89817e2ae19a7f530e9e`  
		Last Modified: Tue, 13 Feb 2024 01:40:41 GMT  
		Size: 223.0 MB (222958232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:eb57f9191ba8aabb66e63d5f20390157c9437e777e1563bf766fb89cee6b07c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203454595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66148c397cce7d44b43567edbcbb720714c1f3d2ccfa306cc6fcb6b6edbd83c1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:20 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Wed, 31 Jan 2024 22:44:20 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 03:04:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 03:04:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 01 Feb 2024 03:04:42 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 01 Feb 2024 03:04:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 03:04:43 GMT
WORKDIR /root
# Thu, 01 Feb 2024 19:06:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=253390a14f6f5d764c82df4b2c2cf18a1c30a8e1fe0849448cc4fedabaaf1d48;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ee647813284e4464a46ffcf9af36ef8d891494056238f7b52a0485fcdefedb5a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9818a37dd39e8e91a0159bdd2522213f9d36bbd99b715465b4606190e6ae41c3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c691e45c53bf0dcc2ff82acf359b96c8a73a1bd896d6ce6e6e94a651eec4d5`  
		Last Modified: Thu, 01 Feb 2024 03:05:39 GMT  
		Size: 49.1 MB (49137166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6767c2ba959af85f7303ac2aeea7320eec31783ce5fa0dc98b455128ba2f64e1`  
		Last Modified: Thu, 01 Feb 2024 03:05:31 GMT  
		Size: 1.2 MB (1227381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a64872379a7bbac3d173a9bf19ad8c24d9514b92f07d3c1ad105a56cbe828fc`  
		Last Modified: Thu, 01 Feb 2024 19:07:34 GMT  
		Size: 128.3 MB (128348483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:fb50d982e8c6b72b72f1baa3c9665a1e9e33f798286290f84616daa6a2ef18ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307180647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dc285d808d636fc2eb640b793fd5564c81b30b19c6c0d137ce20a4b0697e3e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:35:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:35:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Feb 2024 04:35:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Feb 2024 04:35:23 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 04:35:23 GMT
WORKDIR /root
# Tue, 13 Feb 2024 04:35:36 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=253390a14f6f5d764c82df4b2c2cf18a1c30a8e1fe0849448cc4fedabaaf1d48;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ee647813284e4464a46ffcf9af36ef8d891494056238f7b52a0485fcdefedb5a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9818a37dd39e8e91a0159bdd2522213f9d36bbd99b715465b4606190e6ae41c3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f58fc76365edd64e5a8d822fa1fba2b32deb0c12a083c452d19e5c3d1aa770`  
		Last Modified: Tue, 13 Feb 2024 04:36:20 GMT  
		Size: 54.3 MB (54320746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6998d8e36bbe59eb1c78edfc2d292587d2e1fc39c4ed0c71cde8ad747aa4599`  
		Last Modified: Tue, 13 Feb 2024 04:36:15 GMT  
		Size: 1.5 MB (1493769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587f3b27785c1174ff73a1b839057bb996e2a60c10850e70009e88b482b93a32`  
		Last Modified: Tue, 13 Feb 2024 04:36:38 GMT  
		Size: 222.2 MB (222209769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
