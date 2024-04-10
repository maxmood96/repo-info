<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.3`](#dart33)
-	[`dart:3.3-sdk`](#dart33-sdk)
-	[`dart:3.3.3`](#dart333)
-	[`dart:3.3.3-sdk`](#dart333-sdk)
-	[`dart:3.4.0-282.1.beta`](#dart340-2821beta)
-	[`dart:3.4.0-282.1.beta-sdk`](#dart340-2821beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:1c65952b569841bb94f765744ea471913a23390d1637db4df27ffec383812faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3` - linux; amd64

```console
$ docker pull dart@sha256:4d5f3ec5071311cb7892988252ca60236e41568bfa9582bb76989429c37da1c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314033524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cbfd4a34f5f339dd6e147c0c2e381f3e7f0a03a4c53626c3148fc0a7b911b3b`
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
# Wed, 10 Apr 2024 05:41:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:4024c46beb4b0c253d1bb996062eddf49b27c225e8e8bf6471bf23c4d2fc923e`  
		Last Modified: Wed, 10 Apr 2024 05:42:03 GMT  
		Size: 228.4 MB (228447592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d315e825055d925613c2bf0b638f6f16bea65c4a7f9632c8b4d7824c9245f51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206887870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc21d9a9b1bc9ec7066c1ab5e5bddcd2c1a990ee1902f90656fa65fb1b61870`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:24:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 12 Mar 2024 02:24:58 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 12 Mar 2024 02:24:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 02:24:58 GMT
WORKDIR /root
# Wed, 27 Mar 2024 19:09:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675fea3a3b4028a3e4436d6f6a9d0f9a0d43f0f56f725fb4a19d541ee7cfaa9a`  
		Last Modified: Tue, 12 Mar 2024 02:25:58 GMT  
		Size: 49.1 MB (49134287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f881161892b884843f3b1df0a6bf79ee38d0730fc2fa606f61608242d16a87`  
		Last Modified: Tue, 12 Mar 2024 02:25:49 GMT  
		Size: 1.2 MB (1227369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7344debcd6e52652e04fa2fe649621b10d4f049252f8561c98b1f8c7a4b73e63`  
		Last Modified: Wed, 27 Mar 2024 19:10:43 GMT  
		Size: 131.8 MB (131809489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:47dc4f15f878c03b36527c7c7deaf7dbcedda7a8695713e1adb602e0108eb566
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312690337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa04524f154a849c3374cf8f6ed8f4d0a9aeb71341b6fdf0fbda73291baaa156`
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
# Wed, 10 Apr 2024 05:10:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:aeb35d2a280ce8cc4152aadb879eee22d82c8bb07bd0f93b63331d3f9a44f46e`  
		Last Modified: Wed, 10 Apr 2024 05:12:10 GMT  
		Size: 227.7 MB (227711606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3-sdk`

```console
$ docker pull dart@sha256:1c65952b569841bb94f765744ea471913a23390d1637db4df27ffec383812faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3-sdk` - linux; amd64

```console
$ docker pull dart@sha256:4d5f3ec5071311cb7892988252ca60236e41568bfa9582bb76989429c37da1c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314033524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cbfd4a34f5f339dd6e147c0c2e381f3e7f0a03a4c53626c3148fc0a7b911b3b`
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
# Wed, 10 Apr 2024 05:41:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:4024c46beb4b0c253d1bb996062eddf49b27c225e8e8bf6471bf23c4d2fc923e`  
		Last Modified: Wed, 10 Apr 2024 05:42:03 GMT  
		Size: 228.4 MB (228447592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d315e825055d925613c2bf0b638f6f16bea65c4a7f9632c8b4d7824c9245f51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206887870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc21d9a9b1bc9ec7066c1ab5e5bddcd2c1a990ee1902f90656fa65fb1b61870`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:24:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 12 Mar 2024 02:24:58 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 12 Mar 2024 02:24:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 02:24:58 GMT
WORKDIR /root
# Wed, 27 Mar 2024 19:09:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675fea3a3b4028a3e4436d6f6a9d0f9a0d43f0f56f725fb4a19d541ee7cfaa9a`  
		Last Modified: Tue, 12 Mar 2024 02:25:58 GMT  
		Size: 49.1 MB (49134287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f881161892b884843f3b1df0a6bf79ee38d0730fc2fa606f61608242d16a87`  
		Last Modified: Tue, 12 Mar 2024 02:25:49 GMT  
		Size: 1.2 MB (1227369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7344debcd6e52652e04fa2fe649621b10d4f049252f8561c98b1f8c7a4b73e63`  
		Last Modified: Wed, 27 Mar 2024 19:10:43 GMT  
		Size: 131.8 MB (131809489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:47dc4f15f878c03b36527c7c7deaf7dbcedda7a8695713e1adb602e0108eb566
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312690337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa04524f154a849c3374cf8f6ed8f4d0a9aeb71341b6fdf0fbda73291baaa156`
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
# Wed, 10 Apr 2024 05:10:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:aeb35d2a280ce8cc4152aadb879eee22d82c8bb07bd0f93b63331d3f9a44f46e`  
		Last Modified: Wed, 10 Apr 2024 05:12:10 GMT  
		Size: 227.7 MB (227711606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.3`

```console
$ docker pull dart@sha256:1c65952b569841bb94f765744ea471913a23390d1637db4df27ffec383812faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.3` - linux; amd64

```console
$ docker pull dart@sha256:4d5f3ec5071311cb7892988252ca60236e41568bfa9582bb76989429c37da1c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314033524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cbfd4a34f5f339dd6e147c0c2e381f3e7f0a03a4c53626c3148fc0a7b911b3b`
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
# Wed, 10 Apr 2024 05:41:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:4024c46beb4b0c253d1bb996062eddf49b27c225e8e8bf6471bf23c4d2fc923e`  
		Last Modified: Wed, 10 Apr 2024 05:42:03 GMT  
		Size: 228.4 MB (228447592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.3` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d315e825055d925613c2bf0b638f6f16bea65c4a7f9632c8b4d7824c9245f51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206887870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc21d9a9b1bc9ec7066c1ab5e5bddcd2c1a990ee1902f90656fa65fb1b61870`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:24:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 12 Mar 2024 02:24:58 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 12 Mar 2024 02:24:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 02:24:58 GMT
WORKDIR /root
# Wed, 27 Mar 2024 19:09:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675fea3a3b4028a3e4436d6f6a9d0f9a0d43f0f56f725fb4a19d541ee7cfaa9a`  
		Last Modified: Tue, 12 Mar 2024 02:25:58 GMT  
		Size: 49.1 MB (49134287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f881161892b884843f3b1df0a6bf79ee38d0730fc2fa606f61608242d16a87`  
		Last Modified: Tue, 12 Mar 2024 02:25:49 GMT  
		Size: 1.2 MB (1227369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7344debcd6e52652e04fa2fe649621b10d4f049252f8561c98b1f8c7a4b73e63`  
		Last Modified: Wed, 27 Mar 2024 19:10:43 GMT  
		Size: 131.8 MB (131809489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:47dc4f15f878c03b36527c7c7deaf7dbcedda7a8695713e1adb602e0108eb566
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312690337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa04524f154a849c3374cf8f6ed8f4d0a9aeb71341b6fdf0fbda73291baaa156`
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
# Wed, 10 Apr 2024 05:10:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:aeb35d2a280ce8cc4152aadb879eee22d82c8bb07bd0f93b63331d3f9a44f46e`  
		Last Modified: Wed, 10 Apr 2024 05:12:10 GMT  
		Size: 227.7 MB (227711606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.3-sdk`

```console
$ docker pull dart@sha256:1c65952b569841bb94f765744ea471913a23390d1637db4df27ffec383812faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.3-sdk` - linux; amd64

```console
$ docker pull dart@sha256:4d5f3ec5071311cb7892988252ca60236e41568bfa9582bb76989429c37da1c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314033524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cbfd4a34f5f339dd6e147c0c2e381f3e7f0a03a4c53626c3148fc0a7b911b3b`
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
# Wed, 10 Apr 2024 05:41:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:4024c46beb4b0c253d1bb996062eddf49b27c225e8e8bf6471bf23c4d2fc923e`  
		Last Modified: Wed, 10 Apr 2024 05:42:03 GMT  
		Size: 228.4 MB (228447592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d315e825055d925613c2bf0b638f6f16bea65c4a7f9632c8b4d7824c9245f51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206887870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc21d9a9b1bc9ec7066c1ab5e5bddcd2c1a990ee1902f90656fa65fb1b61870`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:24:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 12 Mar 2024 02:24:58 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 12 Mar 2024 02:24:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 02:24:58 GMT
WORKDIR /root
# Wed, 27 Mar 2024 19:09:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675fea3a3b4028a3e4436d6f6a9d0f9a0d43f0f56f725fb4a19d541ee7cfaa9a`  
		Last Modified: Tue, 12 Mar 2024 02:25:58 GMT  
		Size: 49.1 MB (49134287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f881161892b884843f3b1df0a6bf79ee38d0730fc2fa606f61608242d16a87`  
		Last Modified: Tue, 12 Mar 2024 02:25:49 GMT  
		Size: 1.2 MB (1227369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7344debcd6e52652e04fa2fe649621b10d4f049252f8561c98b1f8c7a4b73e63`  
		Last Modified: Wed, 27 Mar 2024 19:10:43 GMT  
		Size: 131.8 MB (131809489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:47dc4f15f878c03b36527c7c7deaf7dbcedda7a8695713e1adb602e0108eb566
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312690337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa04524f154a849c3374cf8f6ed8f4d0a9aeb71341b6fdf0fbda73291baaa156`
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
# Wed, 10 Apr 2024 05:10:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:aeb35d2a280ce8cc4152aadb879eee22d82c8bb07bd0f93b63331d3f9a44f46e`  
		Last Modified: Wed, 10 Apr 2024 05:12:10 GMT  
		Size: 227.7 MB (227711606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.3.3`

```console
$ docker pull dart@sha256:1c65952b569841bb94f765744ea471913a23390d1637db4df27ffec383812faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.3.3` - linux; amd64

```console
$ docker pull dart@sha256:4d5f3ec5071311cb7892988252ca60236e41568bfa9582bb76989429c37da1c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314033524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cbfd4a34f5f339dd6e147c0c2e381f3e7f0a03a4c53626c3148fc0a7b911b3b`
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
# Wed, 10 Apr 2024 05:41:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:4024c46beb4b0c253d1bb996062eddf49b27c225e8e8bf6471bf23c4d2fc923e`  
		Last Modified: Wed, 10 Apr 2024 05:42:03 GMT  
		Size: 228.4 MB (228447592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.3.3` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d315e825055d925613c2bf0b638f6f16bea65c4a7f9632c8b4d7824c9245f51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206887870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc21d9a9b1bc9ec7066c1ab5e5bddcd2c1a990ee1902f90656fa65fb1b61870`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:24:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 12 Mar 2024 02:24:58 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 12 Mar 2024 02:24:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 02:24:58 GMT
WORKDIR /root
# Wed, 27 Mar 2024 19:09:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675fea3a3b4028a3e4436d6f6a9d0f9a0d43f0f56f725fb4a19d541ee7cfaa9a`  
		Last Modified: Tue, 12 Mar 2024 02:25:58 GMT  
		Size: 49.1 MB (49134287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f881161892b884843f3b1df0a6bf79ee38d0730fc2fa606f61608242d16a87`  
		Last Modified: Tue, 12 Mar 2024 02:25:49 GMT  
		Size: 1.2 MB (1227369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7344debcd6e52652e04fa2fe649621b10d4f049252f8561c98b1f8c7a4b73e63`  
		Last Modified: Wed, 27 Mar 2024 19:10:43 GMT  
		Size: 131.8 MB (131809489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.3.3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:47dc4f15f878c03b36527c7c7deaf7dbcedda7a8695713e1adb602e0108eb566
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312690337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa04524f154a849c3374cf8f6ed8f4d0a9aeb71341b6fdf0fbda73291baaa156`
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
# Wed, 10 Apr 2024 05:10:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:aeb35d2a280ce8cc4152aadb879eee22d82c8bb07bd0f93b63331d3f9a44f46e`  
		Last Modified: Wed, 10 Apr 2024 05:12:10 GMT  
		Size: 227.7 MB (227711606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.3.3-sdk`

```console
$ docker pull dart@sha256:1c65952b569841bb94f765744ea471913a23390d1637db4df27ffec383812faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.3.3-sdk` - linux; amd64

```console
$ docker pull dart@sha256:4d5f3ec5071311cb7892988252ca60236e41568bfa9582bb76989429c37da1c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314033524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cbfd4a34f5f339dd6e147c0c2e381f3e7f0a03a4c53626c3148fc0a7b911b3b`
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
# Wed, 10 Apr 2024 05:41:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:4024c46beb4b0c253d1bb996062eddf49b27c225e8e8bf6471bf23c4d2fc923e`  
		Last Modified: Wed, 10 Apr 2024 05:42:03 GMT  
		Size: 228.4 MB (228447592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.3.3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d315e825055d925613c2bf0b638f6f16bea65c4a7f9632c8b4d7824c9245f51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206887870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc21d9a9b1bc9ec7066c1ab5e5bddcd2c1a990ee1902f90656fa65fb1b61870`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:24:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 12 Mar 2024 02:24:58 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 12 Mar 2024 02:24:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 02:24:58 GMT
WORKDIR /root
# Wed, 27 Mar 2024 19:09:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675fea3a3b4028a3e4436d6f6a9d0f9a0d43f0f56f725fb4a19d541ee7cfaa9a`  
		Last Modified: Tue, 12 Mar 2024 02:25:58 GMT  
		Size: 49.1 MB (49134287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f881161892b884843f3b1df0a6bf79ee38d0730fc2fa606f61608242d16a87`  
		Last Modified: Tue, 12 Mar 2024 02:25:49 GMT  
		Size: 1.2 MB (1227369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7344debcd6e52652e04fa2fe649621b10d4f049252f8561c98b1f8c7a4b73e63`  
		Last Modified: Wed, 27 Mar 2024 19:10:43 GMT  
		Size: 131.8 MB (131809489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.3.3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:47dc4f15f878c03b36527c7c7deaf7dbcedda7a8695713e1adb602e0108eb566
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312690337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa04524f154a849c3374cf8f6ed8f4d0a9aeb71341b6fdf0fbda73291baaa156`
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
# Wed, 10 Apr 2024 05:10:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:aeb35d2a280ce8cc4152aadb879eee22d82c8bb07bd0f93b63331d3f9a44f46e`  
		Last Modified: Wed, 10 Apr 2024 05:12:10 GMT  
		Size: 227.7 MB (227711606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.4.0-282.1.beta`

```console
$ docker pull dart@sha256:8d65feb62b253b7efad8105e0c488f0832f653631cdd6842c20a4736ad1d7e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.4.0-282.1.beta` - linux; amd64

```console
$ docker pull dart@sha256:4a758f0a8890bcfed87d49fd64948efc047a23b5fac4587c206788c1d196c2d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (322039567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25990f9aa22a9b2ead99bd0837a9b8fcba8cbee44965f6392d31c3978eb89f62`
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
# Wed, 10 Apr 2024 05:41:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c0663d3de1ea0fd68ea2d1bbf2df06ce32e6b869c8a895881f9d431ab14ab18;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a74e19878ad8aef2945995150d7d78167a346d9f4d20df6a0b50dae9fb4ca942;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f63d89b998c8b34fcb27f3d522a229ab7c5b3233bc30bb6f4d98bc12dd921435;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.4.0-282.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:ef705221d07fa0fbab6d1e533a6f21df042296b64e791782aa5a56b2ef3696f1`  
		Last Modified: Wed, 10 Apr 2024 05:42:55 GMT  
		Size: 236.5 MB (236453635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.4.0-282.1.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:421a4b03ede67dd27333e76dbc362a018dc6d43f0af78ecd8e61fac94dcddf9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.8 MB (208835758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c288ef1cec89f4e0ca6eb04e1947fec44986b814c02ae63d65781ef10b7e4b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:24:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 12 Mar 2024 02:24:58 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 12 Mar 2024 02:24:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 02:24:58 GMT
WORKDIR /root
# Fri, 05 Apr 2024 22:04:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c0663d3de1ea0fd68ea2d1bbf2df06ce32e6b869c8a895881f9d431ab14ab18;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a74e19878ad8aef2945995150d7d78167a346d9f4d20df6a0b50dae9fb4ca942;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f63d89b998c8b34fcb27f3d522a229ab7c5b3233bc30bb6f4d98bc12dd921435;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.4.0-282.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675fea3a3b4028a3e4436d6f6a9d0f9a0d43f0f56f725fb4a19d541ee7cfaa9a`  
		Last Modified: Tue, 12 Mar 2024 02:25:58 GMT  
		Size: 49.1 MB (49134287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f881161892b884843f3b1df0a6bf79ee38d0730fc2fa606f61608242d16a87`  
		Last Modified: Tue, 12 Mar 2024 02:25:49 GMT  
		Size: 1.2 MB (1227369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b03d9d1b0f3b7592c4ce03af06d538cabe3cd80e5580843fc51b26a8b4e011`  
		Last Modified: Fri, 05 Apr 2024 22:05:47 GMT  
		Size: 133.8 MB (133757377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.4.0-282.1.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4d8755f84da57999c0c3f1de19c7667b316d47639059675207cc8c7457a74af9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.7 MB (320703588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ced326c23fc942ca3ad02c8b58650cec1e4d701fedf45b24d661f43f117d69c`
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
# Wed, 10 Apr 2024 05:11:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c0663d3de1ea0fd68ea2d1bbf2df06ce32e6b869c8a895881f9d431ab14ab18;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a74e19878ad8aef2945995150d7d78167a346d9f4d20df6a0b50dae9fb4ca942;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f63d89b998c8b34fcb27f3d522a229ab7c5b3233bc30bb6f4d98bc12dd921435;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.4.0-282.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:8480dfd720116eff8a18f3348c17f2db40a2307ad7520d47252d57b6979067ca`  
		Last Modified: Wed, 10 Apr 2024 05:12:56 GMT  
		Size: 235.7 MB (235724857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.4.0-282.1.beta-sdk`

```console
$ docker pull dart@sha256:8d65feb62b253b7efad8105e0c488f0832f653631cdd6842c20a4736ad1d7e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.4.0-282.1.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:4a758f0a8890bcfed87d49fd64948efc047a23b5fac4587c206788c1d196c2d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (322039567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25990f9aa22a9b2ead99bd0837a9b8fcba8cbee44965f6392d31c3978eb89f62`
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
# Wed, 10 Apr 2024 05:41:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c0663d3de1ea0fd68ea2d1bbf2df06ce32e6b869c8a895881f9d431ab14ab18;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a74e19878ad8aef2945995150d7d78167a346d9f4d20df6a0b50dae9fb4ca942;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f63d89b998c8b34fcb27f3d522a229ab7c5b3233bc30bb6f4d98bc12dd921435;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.4.0-282.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:ef705221d07fa0fbab6d1e533a6f21df042296b64e791782aa5a56b2ef3696f1`  
		Last Modified: Wed, 10 Apr 2024 05:42:55 GMT  
		Size: 236.5 MB (236453635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.4.0-282.1.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:421a4b03ede67dd27333e76dbc362a018dc6d43f0af78ecd8e61fac94dcddf9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.8 MB (208835758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c288ef1cec89f4e0ca6eb04e1947fec44986b814c02ae63d65781ef10b7e4b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:24:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 12 Mar 2024 02:24:58 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 12 Mar 2024 02:24:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 02:24:58 GMT
WORKDIR /root
# Fri, 05 Apr 2024 22:04:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c0663d3de1ea0fd68ea2d1bbf2df06ce32e6b869c8a895881f9d431ab14ab18;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a74e19878ad8aef2945995150d7d78167a346d9f4d20df6a0b50dae9fb4ca942;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f63d89b998c8b34fcb27f3d522a229ab7c5b3233bc30bb6f4d98bc12dd921435;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.4.0-282.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675fea3a3b4028a3e4436d6f6a9d0f9a0d43f0f56f725fb4a19d541ee7cfaa9a`  
		Last Modified: Tue, 12 Mar 2024 02:25:58 GMT  
		Size: 49.1 MB (49134287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f881161892b884843f3b1df0a6bf79ee38d0730fc2fa606f61608242d16a87`  
		Last Modified: Tue, 12 Mar 2024 02:25:49 GMT  
		Size: 1.2 MB (1227369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b03d9d1b0f3b7592c4ce03af06d538cabe3cd80e5580843fc51b26a8b4e011`  
		Last Modified: Fri, 05 Apr 2024 22:05:47 GMT  
		Size: 133.8 MB (133757377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.4.0-282.1.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4d8755f84da57999c0c3f1de19c7667b316d47639059675207cc8c7457a74af9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.7 MB (320703588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ced326c23fc942ca3ad02c8b58650cec1e4d701fedf45b24d661f43f117d69c`
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
# Wed, 10 Apr 2024 05:11:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c0663d3de1ea0fd68ea2d1bbf2df06ce32e6b869c8a895881f9d431ab14ab18;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a74e19878ad8aef2945995150d7d78167a346d9f4d20df6a0b50dae9fb4ca942;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f63d89b998c8b34fcb27f3d522a229ab7c5b3233bc30bb6f4d98bc12dd921435;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.4.0-282.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:8480dfd720116eff8a18f3348c17f2db40a2307ad7520d47252d57b6979067ca`  
		Last Modified: Wed, 10 Apr 2024 05:12:56 GMT  
		Size: 235.7 MB (235724857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta`

```console
$ docker pull dart@sha256:8d65feb62b253b7efad8105e0c488f0832f653631cdd6842c20a4736ad1d7e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:4a758f0a8890bcfed87d49fd64948efc047a23b5fac4587c206788c1d196c2d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (322039567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25990f9aa22a9b2ead99bd0837a9b8fcba8cbee44965f6392d31c3978eb89f62`
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
# Wed, 10 Apr 2024 05:41:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c0663d3de1ea0fd68ea2d1bbf2df06ce32e6b869c8a895881f9d431ab14ab18;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a74e19878ad8aef2945995150d7d78167a346d9f4d20df6a0b50dae9fb4ca942;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f63d89b998c8b34fcb27f3d522a229ab7c5b3233bc30bb6f4d98bc12dd921435;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.4.0-282.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:ef705221d07fa0fbab6d1e533a6f21df042296b64e791782aa5a56b2ef3696f1`  
		Last Modified: Wed, 10 Apr 2024 05:42:55 GMT  
		Size: 236.5 MB (236453635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:421a4b03ede67dd27333e76dbc362a018dc6d43f0af78ecd8e61fac94dcddf9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.8 MB (208835758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c288ef1cec89f4e0ca6eb04e1947fec44986b814c02ae63d65781ef10b7e4b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:24:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 12 Mar 2024 02:24:58 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 12 Mar 2024 02:24:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 02:24:58 GMT
WORKDIR /root
# Fri, 05 Apr 2024 22:04:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c0663d3de1ea0fd68ea2d1bbf2df06ce32e6b869c8a895881f9d431ab14ab18;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a74e19878ad8aef2945995150d7d78167a346d9f4d20df6a0b50dae9fb4ca942;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f63d89b998c8b34fcb27f3d522a229ab7c5b3233bc30bb6f4d98bc12dd921435;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.4.0-282.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675fea3a3b4028a3e4436d6f6a9d0f9a0d43f0f56f725fb4a19d541ee7cfaa9a`  
		Last Modified: Tue, 12 Mar 2024 02:25:58 GMT  
		Size: 49.1 MB (49134287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f881161892b884843f3b1df0a6bf79ee38d0730fc2fa606f61608242d16a87`  
		Last Modified: Tue, 12 Mar 2024 02:25:49 GMT  
		Size: 1.2 MB (1227369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b03d9d1b0f3b7592c4ce03af06d538cabe3cd80e5580843fc51b26a8b4e011`  
		Last Modified: Fri, 05 Apr 2024 22:05:47 GMT  
		Size: 133.8 MB (133757377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4d8755f84da57999c0c3f1de19c7667b316d47639059675207cc8c7457a74af9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.7 MB (320703588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ced326c23fc942ca3ad02c8b58650cec1e4d701fedf45b24d661f43f117d69c`
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
# Wed, 10 Apr 2024 05:11:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c0663d3de1ea0fd68ea2d1bbf2df06ce32e6b869c8a895881f9d431ab14ab18;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a74e19878ad8aef2945995150d7d78167a346d9f4d20df6a0b50dae9fb4ca942;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f63d89b998c8b34fcb27f3d522a229ab7c5b3233bc30bb6f4d98bc12dd921435;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.4.0-282.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:8480dfd720116eff8a18f3348c17f2db40a2307ad7520d47252d57b6979067ca`  
		Last Modified: Wed, 10 Apr 2024 05:12:56 GMT  
		Size: 235.7 MB (235724857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:8d65feb62b253b7efad8105e0c488f0832f653631cdd6842c20a4736ad1d7e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:4a758f0a8890bcfed87d49fd64948efc047a23b5fac4587c206788c1d196c2d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (322039567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25990f9aa22a9b2ead99bd0837a9b8fcba8cbee44965f6392d31c3978eb89f62`
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
# Wed, 10 Apr 2024 05:41:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c0663d3de1ea0fd68ea2d1bbf2df06ce32e6b869c8a895881f9d431ab14ab18;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a74e19878ad8aef2945995150d7d78167a346d9f4d20df6a0b50dae9fb4ca942;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f63d89b998c8b34fcb27f3d522a229ab7c5b3233bc30bb6f4d98bc12dd921435;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.4.0-282.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:ef705221d07fa0fbab6d1e533a6f21df042296b64e791782aa5a56b2ef3696f1`  
		Last Modified: Wed, 10 Apr 2024 05:42:55 GMT  
		Size: 236.5 MB (236453635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:421a4b03ede67dd27333e76dbc362a018dc6d43f0af78ecd8e61fac94dcddf9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.8 MB (208835758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c288ef1cec89f4e0ca6eb04e1947fec44986b814c02ae63d65781ef10b7e4b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:24:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 12 Mar 2024 02:24:58 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 12 Mar 2024 02:24:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 02:24:58 GMT
WORKDIR /root
# Fri, 05 Apr 2024 22:04:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c0663d3de1ea0fd68ea2d1bbf2df06ce32e6b869c8a895881f9d431ab14ab18;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a74e19878ad8aef2945995150d7d78167a346d9f4d20df6a0b50dae9fb4ca942;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f63d89b998c8b34fcb27f3d522a229ab7c5b3233bc30bb6f4d98bc12dd921435;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.4.0-282.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675fea3a3b4028a3e4436d6f6a9d0f9a0d43f0f56f725fb4a19d541ee7cfaa9a`  
		Last Modified: Tue, 12 Mar 2024 02:25:58 GMT  
		Size: 49.1 MB (49134287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f881161892b884843f3b1df0a6bf79ee38d0730fc2fa606f61608242d16a87`  
		Last Modified: Tue, 12 Mar 2024 02:25:49 GMT  
		Size: 1.2 MB (1227369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b03d9d1b0f3b7592c4ce03af06d538cabe3cd80e5580843fc51b26a8b4e011`  
		Last Modified: Fri, 05 Apr 2024 22:05:47 GMT  
		Size: 133.8 MB (133757377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4d8755f84da57999c0c3f1de19c7667b316d47639059675207cc8c7457a74af9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.7 MB (320703588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ced326c23fc942ca3ad02c8b58650cec1e4d701fedf45b24d661f43f117d69c`
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
# Wed, 10 Apr 2024 05:11:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c0663d3de1ea0fd68ea2d1bbf2df06ce32e6b869c8a895881f9d431ab14ab18;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a74e19878ad8aef2945995150d7d78167a346d9f4d20df6a0b50dae9fb4ca942;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f63d89b998c8b34fcb27f3d522a229ab7c5b3233bc30bb6f4d98bc12dd921435;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.4.0-282.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:8480dfd720116eff8a18f3348c17f2db40a2307ad7520d47252d57b6979067ca`  
		Last Modified: Wed, 10 Apr 2024 05:12:56 GMT  
		Size: 235.7 MB (235724857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:latest`

```console
$ docker pull dart@sha256:1c65952b569841bb94f765744ea471913a23390d1637db4df27ffec383812faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:4d5f3ec5071311cb7892988252ca60236e41568bfa9582bb76989429c37da1c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314033524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cbfd4a34f5f339dd6e147c0c2e381f3e7f0a03a4c53626c3148fc0a7b911b3b`
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
# Wed, 10 Apr 2024 05:41:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:4024c46beb4b0c253d1bb996062eddf49b27c225e8e8bf6471bf23c4d2fc923e`  
		Last Modified: Wed, 10 Apr 2024 05:42:03 GMT  
		Size: 228.4 MB (228447592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d315e825055d925613c2bf0b638f6f16bea65c4a7f9632c8b4d7824c9245f51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206887870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc21d9a9b1bc9ec7066c1ab5e5bddcd2c1a990ee1902f90656fa65fb1b61870`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:24:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 12 Mar 2024 02:24:58 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 12 Mar 2024 02:24:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 02:24:58 GMT
WORKDIR /root
# Wed, 27 Mar 2024 19:09:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675fea3a3b4028a3e4436d6f6a9d0f9a0d43f0f56f725fb4a19d541ee7cfaa9a`  
		Last Modified: Tue, 12 Mar 2024 02:25:58 GMT  
		Size: 49.1 MB (49134287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f881161892b884843f3b1df0a6bf79ee38d0730fc2fa606f61608242d16a87`  
		Last Modified: Tue, 12 Mar 2024 02:25:49 GMT  
		Size: 1.2 MB (1227369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7344debcd6e52652e04fa2fe649621b10d4f049252f8561c98b1f8c7a4b73e63`  
		Last Modified: Wed, 27 Mar 2024 19:10:43 GMT  
		Size: 131.8 MB (131809489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:47dc4f15f878c03b36527c7c7deaf7dbcedda7a8695713e1adb602e0108eb566
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312690337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa04524f154a849c3374cf8f6ed8f4d0a9aeb71341b6fdf0fbda73291baaa156`
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
# Wed, 10 Apr 2024 05:10:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:aeb35d2a280ce8cc4152aadb879eee22d82c8bb07bd0f93b63331d3f9a44f46e`  
		Last Modified: Wed, 10 Apr 2024 05:12:10 GMT  
		Size: 227.7 MB (227711606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:sdk`

```console
$ docker pull dart@sha256:1c65952b569841bb94f765744ea471913a23390d1637db4df27ffec383812faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:4d5f3ec5071311cb7892988252ca60236e41568bfa9582bb76989429c37da1c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314033524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cbfd4a34f5f339dd6e147c0c2e381f3e7f0a03a4c53626c3148fc0a7b911b3b`
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
# Wed, 10 Apr 2024 05:41:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:4024c46beb4b0c253d1bb996062eddf49b27c225e8e8bf6471bf23c4d2fc923e`  
		Last Modified: Wed, 10 Apr 2024 05:42:03 GMT  
		Size: 228.4 MB (228447592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d315e825055d925613c2bf0b638f6f16bea65c4a7f9632c8b4d7824c9245f51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206887870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc21d9a9b1bc9ec7066c1ab5e5bddcd2c1a990ee1902f90656fa65fb1b61870`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:24:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 12 Mar 2024 02:24:58 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 12 Mar 2024 02:24:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 02:24:58 GMT
WORKDIR /root
# Wed, 27 Mar 2024 19:09:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675fea3a3b4028a3e4436d6f6a9d0f9a0d43f0f56f725fb4a19d541ee7cfaa9a`  
		Last Modified: Tue, 12 Mar 2024 02:25:58 GMT  
		Size: 49.1 MB (49134287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f881161892b884843f3b1df0a6bf79ee38d0730fc2fa606f61608242d16a87`  
		Last Modified: Tue, 12 Mar 2024 02:25:49 GMT  
		Size: 1.2 MB (1227369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7344debcd6e52652e04fa2fe649621b10d4f049252f8561c98b1f8c7a4b73e63`  
		Last Modified: Wed, 27 Mar 2024 19:10:43 GMT  
		Size: 131.8 MB (131809489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:47dc4f15f878c03b36527c7c7deaf7dbcedda7a8695713e1adb602e0108eb566
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312690337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa04524f154a849c3374cf8f6ed8f4d0a9aeb71341b6fdf0fbda73291baaa156`
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
# Wed, 10 Apr 2024 05:10:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:aeb35d2a280ce8cc4152aadb879eee22d82c8bb07bd0f93b63331d3f9a44f46e`  
		Last Modified: Wed, 10 Apr 2024 05:12:10 GMT  
		Size: 227.7 MB (227711606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable`

```console
$ docker pull dart@sha256:1c65952b569841bb94f765744ea471913a23390d1637db4df27ffec383812faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:4d5f3ec5071311cb7892988252ca60236e41568bfa9582bb76989429c37da1c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314033524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cbfd4a34f5f339dd6e147c0c2e381f3e7f0a03a4c53626c3148fc0a7b911b3b`
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
# Wed, 10 Apr 2024 05:41:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:4024c46beb4b0c253d1bb996062eddf49b27c225e8e8bf6471bf23c4d2fc923e`  
		Last Modified: Wed, 10 Apr 2024 05:42:03 GMT  
		Size: 228.4 MB (228447592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d315e825055d925613c2bf0b638f6f16bea65c4a7f9632c8b4d7824c9245f51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206887870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc21d9a9b1bc9ec7066c1ab5e5bddcd2c1a990ee1902f90656fa65fb1b61870`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:24:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 12 Mar 2024 02:24:58 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 12 Mar 2024 02:24:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 02:24:58 GMT
WORKDIR /root
# Wed, 27 Mar 2024 19:09:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675fea3a3b4028a3e4436d6f6a9d0f9a0d43f0f56f725fb4a19d541ee7cfaa9a`  
		Last Modified: Tue, 12 Mar 2024 02:25:58 GMT  
		Size: 49.1 MB (49134287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f881161892b884843f3b1df0a6bf79ee38d0730fc2fa606f61608242d16a87`  
		Last Modified: Tue, 12 Mar 2024 02:25:49 GMT  
		Size: 1.2 MB (1227369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7344debcd6e52652e04fa2fe649621b10d4f049252f8561c98b1f8c7a4b73e63`  
		Last Modified: Wed, 27 Mar 2024 19:10:43 GMT  
		Size: 131.8 MB (131809489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:47dc4f15f878c03b36527c7c7deaf7dbcedda7a8695713e1adb602e0108eb566
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312690337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa04524f154a849c3374cf8f6ed8f4d0a9aeb71341b6fdf0fbda73291baaa156`
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
# Wed, 10 Apr 2024 05:10:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:aeb35d2a280ce8cc4152aadb879eee22d82c8bb07bd0f93b63331d3f9a44f46e`  
		Last Modified: Wed, 10 Apr 2024 05:12:10 GMT  
		Size: 227.7 MB (227711606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:1c65952b569841bb94f765744ea471913a23390d1637db4df27ffec383812faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:4d5f3ec5071311cb7892988252ca60236e41568bfa9582bb76989429c37da1c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314033524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cbfd4a34f5f339dd6e147c0c2e381f3e7f0a03a4c53626c3148fc0a7b911b3b`
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
# Wed, 10 Apr 2024 05:41:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:4024c46beb4b0c253d1bb996062eddf49b27c225e8e8bf6471bf23c4d2fc923e`  
		Last Modified: Wed, 10 Apr 2024 05:42:03 GMT  
		Size: 228.4 MB (228447592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d315e825055d925613c2bf0b638f6f16bea65c4a7f9632c8b4d7824c9245f51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206887870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc21d9a9b1bc9ec7066c1ab5e5bddcd2c1a990ee1902f90656fa65fb1b61870`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:24:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 12 Mar 2024 02:24:58 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 12 Mar 2024 02:24:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 02:24:58 GMT
WORKDIR /root
# Wed, 27 Mar 2024 19:09:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675fea3a3b4028a3e4436d6f6a9d0f9a0d43f0f56f725fb4a19d541ee7cfaa9a`  
		Last Modified: Tue, 12 Mar 2024 02:25:58 GMT  
		Size: 49.1 MB (49134287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f881161892b884843f3b1df0a6bf79ee38d0730fc2fa606f61608242d16a87`  
		Last Modified: Tue, 12 Mar 2024 02:25:49 GMT  
		Size: 1.2 MB (1227369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7344debcd6e52652e04fa2fe649621b10d4f049252f8561c98b1f8c7a4b73e63`  
		Last Modified: Wed, 27 Mar 2024 19:10:43 GMT  
		Size: 131.8 MB (131809489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:47dc4f15f878c03b36527c7c7deaf7dbcedda7a8695713e1adb602e0108eb566
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312690337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa04524f154a849c3374cf8f6ed8f4d0a9aeb71341b6fdf0fbda73291baaa156`
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
# Wed, 10 Apr 2024 05:10:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:aeb35d2a280ce8cc4152aadb879eee22d82c8bb07bd0f93b63331d3f9a44f46e`  
		Last Modified: Wed, 10 Apr 2024 05:12:10 GMT  
		Size: 227.7 MB (227711606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
