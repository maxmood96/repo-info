## `dart:beta`

```console
$ docker pull dart@sha256:cea97886b77255bae071d4baf5254d85b956a83c055c3e163c329ff9e87778ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:4ec49e3b9458e1ec1813afa5198c64d1e8deec502bc9c9c09395b0257f2677e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 MB (322069428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d357f0250d098b36fdca0a096410b156b35bf8ccdc99b31755e54973fb5cadee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:40:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:40:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 10 Apr 2024 05:40:48 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 10 Apr 2024 05:40:48 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 05:40:48 GMT
WORKDIR /root
# Thu, 18 Apr 2024 17:51:19 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=7c4652d0d1fe5f375d6d810e98dccaeda02d8dd9251babca4c53b7ec4c20a697;             SDK_ARCH="x64";;         armhf)             DART_SHA256=21d47dbdd97708adca357e780741c216bfeb7a4fcbe158e6cead99ba3c75f002;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e6bf4b25beb84aac39b6a472888230133c0324dd0dc4cf261176f8995fde6e0e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.4.0-282.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c8f42625841a8a89dd36e5148da871b75f04a9ffe853d0275ca4d8f94370d0`  
		Last Modified: Wed, 10 Apr 2024 05:41:41 GMT  
		Size: 54.7 MB (54653850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad97c0bf7e0a5b0e2f6afc6c9598a95b68487c14a57a3fff438ab492cdff5885`  
		Last Modified: Wed, 10 Apr 2024 05:41:33 GMT  
		Size: 1.8 MB (1800724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ae6942b9ea579093bd1f699a606b4d3862db932d5003ca6b2031d7475178df`  
		Last Modified: Thu, 18 Apr 2024 17:53:00 GMT  
		Size: 236.5 MB (236483496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:d1db4f7625db9469caec4422329a25cb0d738b403530031cc213d950f61a9aa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.8 MB (208834208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec26277f09db5d77f0c32c7a5c4d91f19c283357b4d2c465cce497b2738149e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:11 GMT
ADD file:405264a6fec3e83d872f4297605fa82dd8f7a7724cbccbb7ebf06438266aa933 in / 
# Wed, 10 Apr 2024 00:58:12 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:07:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:07:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 10 Apr 2024 07:07:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 10 Apr 2024 07:07:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:07:12 GMT
WORKDIR /root
# Thu, 18 Apr 2024 18:03:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=7c4652d0d1fe5f375d6d810e98dccaeda02d8dd9251babca4c53b7ec4c20a697;             SDK_ARCH="x64";;         armhf)             DART_SHA256=21d47dbdd97708adca357e780741c216bfeb7a4fcbe158e6cead99ba3c75f002;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e6bf4b25beb84aac39b6a472888230133c0324dd0dc4cf261176f8995fde6e0e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.4.0-282.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c774609c4cd3f6537d30d03e0ad1c935b83618698a710164c43debe51dadfd87`  
		Last Modified: Wed, 10 Apr 2024 01:04:25 GMT  
		Size: 24.7 MB (24722923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48db2fd4a97cda4e6d38d613ec7d001fa408fcf2909a662b4bfe04b432129db7`  
		Last Modified: Wed, 10 Apr 2024 07:08:25 GMT  
		Size: 49.1 MB (49133619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50f319582957de8d6f3c90b2900b97fec48377f31f78d9774491e40f4c318aa`  
		Last Modified: Wed, 10 Apr 2024 07:08:12 GMT  
		Size: 1.2 MB (1227374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944faa940f6dac39a28412dce1e7940c8cfd1c648790b8a013040d9945063a42`  
		Last Modified: Thu, 18 Apr 2024 18:05:24 GMT  
		Size: 133.8 MB (133750292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:2343293fd7f0bd73b5dc0b92ed250277bb592b058ad5dbef4cea9444a747baa0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.7 MB (320739583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fab8bdd2e3f9a2f4782fde6c154badccf1bc75f8e5851baf3944d7d161ae9a0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:10:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:10:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 10 Apr 2024 05:10:42 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 10 Apr 2024 05:10:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 05:10:42 GMT
WORKDIR /root
# Thu, 18 Apr 2024 18:03:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=7c4652d0d1fe5f375d6d810e98dccaeda02d8dd9251babca4c53b7ec4c20a697;             SDK_ARCH="x64";;         armhf)             DART_SHA256=21d47dbdd97708adca357e780741c216bfeb7a4fcbe158e6cead99ba3c75f002;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e6bf4b25beb84aac39b6a472888230133c0324dd0dc4cf261176f8995fde6e0e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.4.0-282.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911af322132dafaa481fc7abdb6102f8ca1a90809c49105ea9932927d01dd2a0`  
		Last Modified: Wed, 10 Apr 2024 05:11:51 GMT  
		Size: 54.3 MB (54322806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c11a32dfaef706716ccfd5326eaa26ff711af44ed507b45c9089db9bab3386db`  
		Last Modified: Wed, 10 Apr 2024 05:11:46 GMT  
		Size: 1.5 MB (1493768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f612ffa5cbbb053a290620c2b84673f3e1e9773295d1dd17cde2cd3efe339f2`  
		Last Modified: Thu, 18 Apr 2024 18:05:10 GMT  
		Size: 235.8 MB (235760852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
