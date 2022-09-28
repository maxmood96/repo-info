## `dart:2-sdk`

```console
$ docker pull dart@sha256:d27805f67d8ca7f95b69a0d8635f0c257532797d92f6b2750acf190751f1a991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2-sdk` - linux; amd64

```console
$ docker pull dart@sha256:ec4d4919310a837d2bededf76e4c2d797e9123143a0922cf8b404cc8611e3c08
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271938880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd807bcce5165744ee4b309ab784ee9d1a6a18f63cc8c8a99b808c2055af60b9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:57:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:57:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Sep 2022 03:57:10 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Sep 2022 03:57:10 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 03:57:10 GMT
WORKDIR /root
# Wed, 28 Sep 2022 17:19:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b7f988de7172ef4a626b2f08bd1fb4e00fd369d0002b456c7711d06b7d0a535;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f14ec4fcc222c88dfd5d1fec47ac527ee172e5b974974de9a7c5213922d05e70;             SDK_ARCH="arm";;         arm64)             DART_SHA256=cf220ad62e7ff4fd82fac8f3740ae1170a553b83fe22dfbf5f9d25fa7f607a42;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d63b6474cd1858e80830a661cd94266316317015c29b48065f8ca8f4be032b2`  
		Last Modified: Tue, 13 Sep 2022 03:57:52 GMT  
		Size: 45.1 MB (45076266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b3e6f150bf6765ed0be2d60b823b718ea7bd975a53d61d41868af1dc4ac11e`  
		Last Modified: Tue, 13 Sep 2022 03:57:45 GMT  
		Size: 2.2 MB (2161955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dafb8502472ea3893ee5c7c2e0e918e87744e1f81ba90de0bb327fb9d2c861a3`  
		Last Modified: Wed, 28 Sep 2022 17:20:41 GMT  
		Size: 193.3 MB (193296538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:e395c149cdc1d5f09f6d51ae331b61318f0c5a92cca1b83d757e4446e8335e81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180595318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36ecb1a29cd7aad4981942824c69e6fdfbb4e7d1e184c9179e8ca0f4501c48e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 03:42:37 GMT
ADD file:04b0c48a2d326e2ac4255df4a6165508f0d29d8a32147fb8df6bf9504b8f6b09 in / 
# Tue, 13 Sep 2022 03:42:37 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 07:26:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 07:26:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Sep 2022 07:26:14 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Sep 2022 07:26:14 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 07:26:14 GMT
WORKDIR /root
# Wed, 28 Sep 2022 17:47:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b7f988de7172ef4a626b2f08bd1fb4e00fd369d0002b456c7711d06b7d0a535;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f14ec4fcc222c88dfd5d1fec47ac527ee172e5b974974de9a7c5213922d05e70;             SDK_ARCH="arm";;         arm64)             DART_SHA256=cf220ad62e7ff4fd82fac8f3740ae1170a553b83fe22dfbf5f9d25fa7f607a42;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:43caeee1782255456dd3403ae8e6ba191802c3deb004ca68ce0420b30368995d`  
		Last Modified: Tue, 13 Sep 2022 03:49:46 GMT  
		Size: 26.6 MB (26567059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67b1ef7c0532bd5fe661ea9cbf8603025c7072df6966b5e2eea270252e6dfad`  
		Last Modified: Tue, 13 Sep 2022 07:27:20 GMT  
		Size: 41.0 MB (40963731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6838c05dc76bf1457f69908db62b75bff01a7ad0947fe5d967f458d33a5ef07b`  
		Last Modified: Tue, 13 Sep 2022 07:27:10 GMT  
		Size: 1.3 MB (1288525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6edabed1be06c39bbbcd41d090e1a0e9d115c6ad1c28b79605be2bbd7e91e572`  
		Last Modified: Wed, 28 Sep 2022 17:48:12 GMT  
		Size: 111.8 MB (111776003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:da1c572df3b86d7a7fd4cc0890e7425cd48276e479d0f8d1d5c9b2be62be287b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189554406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe9b4fb99e4c821e791d9676ac7d087a694c8c873fa2ee8e4ec42a7c97cc984`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 05:14:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 05:14:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Sep 2022 05:14:16 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Sep 2022 05:14:17 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 05:14:18 GMT
WORKDIR /root
# Wed, 28 Sep 2022 16:39:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b7f988de7172ef4a626b2f08bd1fb4e00fd369d0002b456c7711d06b7d0a535;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f14ec4fcc222c88dfd5d1fec47ac527ee172e5b974974de9a7c5213922d05e70;             SDK_ARCH="arm";;         arm64)             DART_SHA256=cf220ad62e7ff4fd82fac8f3740ae1170a553b83fe22dfbf5f9d25fa7f607a42;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9a9bed1a37d8212c4127b7f476a6973c996f4cbd08e44efa25b860f6ad06ce`  
		Last Modified: Tue, 13 Sep 2022 05:15:09 GMT  
		Size: 45.0 MB (45003804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889d53a2fc31f3cb8044ed793a36d337b0f8a984b0edc1866293b36a9116b721`  
		Last Modified: Tue, 13 Sep 2022 05:15:03 GMT  
		Size: 1.6 MB (1556381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc50f11ebfc144747cc25c00e26203d0f245b5a11019cd049d46e9ac4ab4bfb2`  
		Last Modified: Wed, 28 Sep 2022 16:40:44 GMT  
		Size: 112.9 MB (112939982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
