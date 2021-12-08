## `dart:2-sdk`

```console
$ docker pull dart@sha256:c13c54d9bc0971cd9d351f96b5a033a31fcdeae82e31b7ed6f989a5034a6c1a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2-sdk` - linux; amd64

```console
$ docker pull dart@sha256:cb6175642c8782084ab253fc57ea49fcee5eb5ab105cd16fdf9989589078c678
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289082090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb21ef57e7308cdf354f4b09cc145cd6d59dc01df8f14b283274c6983a20d27e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 04:02:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 04:02:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 04:02:18 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 04:02:18 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 04:02:19 GMT
WORKDIR /root
# Thu, 02 Dec 2021 04:02:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=49b6a98008ef546cb9c221461529d6c02cf2474bff098e0dc7e4ff1ef0f8a289;             SDK_ARCH="x64";;         armhf)             DART_SHA256=796b64022615ea75f05f20a3d5e7018e52a1d26c06acb1d2b0b2faa5df491a64;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0477fae6fcff58fec18d912537f13d647fa0e137fce23401eea73102dce62351;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.14.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb481969b5bc2bc8729b84d58c0d6699230b0a6bca266a77fc57f272c91c0178`  
		Last Modified: Thu, 02 Dec 2021 04:03:38 GMT  
		Size: 49.6 MB (49583370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90847d193a80622867c2850f98e4da3b6337d0a864cb4cf6d4d7d2e3f2caa7b`  
		Last Modified: Thu, 02 Dec 2021 04:03:27 GMT  
		Size: 2.4 MB (2359141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb8369f9ae06fd1f6bbf0d9892b2dff06dddc55ebe19816f63113da358b81636`  
		Last Modified: Thu, 02 Dec 2021 04:04:05 GMT  
		Size: 210.0 MB (209985850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:cfb2f42f648bf104d807a890358592c1cf07b4a3935e0ac6bd599397fe6faf09
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183685162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8275561b3f87e4a0ccc2f8daab8c97f640759829660046840e811bd32b509ca8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 09:06:21 GMT
ADD file:7b30d743b30e84b21888f23cb7f266caba09db98b7a4c8800abebcf03d28c01d in / 
# Thu, 02 Dec 2021 09:06:22 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 17:39:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 17:39:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 17:39:31 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 17:39:32 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 17:39:32 GMT
WORKDIR /root
# Wed, 08 Dec 2021 19:57:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=53557538f98578d642741c45cbbcaa01b004d1cc61f5fd94a8a426ade26ef580;             SDK_ARCH="x64";;         armhf)             DART_SHA256=22e112cfd0e99bf54ce000a55d63017e322bac9e810b61195d701c785de897f5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=bfa01d1842fccf9e59bfed8edbb3e43921d37b04d4cf1af6a6895e3bc6243000;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2aa85085c98821a25a3058f7fc2c6427064f2228ea8eac904e9e7db4dbdaa01a`  
		Last Modified: Thu, 02 Dec 2021 09:22:26 GMT  
		Size: 22.8 MB (22754365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cba88e2b81c4f12b2ea6f779cb27400c7a946fd8234c4dcaccbd68daa7009b6`  
		Last Modified: Thu, 02 Dec 2021 17:42:16 GMT  
		Size: 44.4 MB (44399226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481e35b1e2bc599c933280bb665519a8cc102dba7301afe868505bbaa5bc183d`  
		Last Modified: Thu, 02 Dec 2021 17:41:51 GMT  
		Size: 1.4 MB (1355908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407852ba04a0bdb23e9b2a8a2fe0e9493a95f3a4f8176ccef6b10365a67ab300`  
		Last Modified: Wed, 08 Dec 2021 20:00:26 GMT  
		Size: 115.2 MB (115175663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:449fe28b9d585fbc8ac7b8b1609192893c683dd3ce47f53512e35587fe230222
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.0 MB (200018576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5defd0de935776d3e159c1d9cb222877660d09e9443a34724945fa295b4e36ce`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:34 GMT
ADD file:83d9e760a84be2bd8754e31e33b3f782b44f6e7b7e02c156f519715c88c40615 in / 
# Thu, 02 Dec 2021 08:08:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:10:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:10:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 10:10:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 10:10:36 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:10:37 GMT
WORKDIR /root
# Thu, 02 Dec 2021 10:10:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=49b6a98008ef546cb9c221461529d6c02cf2474bff098e0dc7e4ff1ef0f8a289;             SDK_ARCH="x64";;         armhf)             DART_SHA256=796b64022615ea75f05f20a3d5e7018e52a1d26c06acb1d2b0b2faa5df491a64;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0477fae6fcff58fec18d912537f13d647fa0e137fce23401eea73102dce62351;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.14.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2a37a2e6ba8cbf21e3950cf7b2455f0af054667b6a35719fb2bd6070973bfa76`  
		Last Modified: Thu, 02 Dec 2021 08:41:37 GMT  
		Size: 25.9 MB (25923144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9514eec777ef806660e5c8a0e2019db098e460e313b3212baad2d9a3c74a04`  
		Last Modified: Thu, 02 Dec 2021 10:11:47 GMT  
		Size: 49.6 MB (49639089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bd4fe19302b8d33de0926bafa96b46c46ec80d6bf5e69467b4b18f388e9e6d`  
		Last Modified: Thu, 02 Dec 2021 10:11:40 GMT  
		Size: 1.6 MB (1631924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4555ca60927478db7f09343b8deb38a64086cdccc97c0ea3a5299e756eef28e3`  
		Last Modified: Thu, 02 Dec 2021 10:11:58 GMT  
		Size: 122.8 MB (122824419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
