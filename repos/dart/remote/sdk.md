## `dart:sdk`

```console
$ docker pull dart@sha256:f0d6115c9c3d7b9bba8961d0ea8aabbbe91bcb14d8097f5f86786161ad8ef8fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:a1be4b9043d3fc83d227529812d432bf93fb66b6f8f283ec0f5c278b17b56af4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276273114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ec444e1b761fb59069a305d60215fe17fed57593f09d0a2e0667d640955f35`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Wed, 12 Jan 2022 22:19:41 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d994bc069ece837ad29462f0e46afbdb6ccce72e82cfe1daa44a83876348bb55`  
		Last Modified: Wed, 12 Jan 2022 22:20:48 GMT  
		Size: 197.2 MB (197176760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:21e63e46d2c279a16a7e0d1181ea668a7b93d58ee2509528c0a497a8a07052db
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183687414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b31b9891f29d102fb2cf97a5e9bb5580edfa99e7209f13c319621f98475cc1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:00:52 GMT
ADD file:1381e18e2847f24ebd16d8e83ad940adeff45aca2c327d4e07d7451816f29420 in / 
# Tue, 21 Dec 2021 02:00:52 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:31:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:31:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 03:31:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 03:31:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 03:31:50 GMT
WORKDIR /root
# Wed, 12 Jan 2022 22:58:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b597e1a6bc27aa2a24a587cb687c9551dfbcfa730a11d48c5a44ff77ff6fdd75`  
		Last Modified: Tue, 21 Dec 2021 02:16:50 GMT  
		Size: 22.8 MB (22754324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724933b2255953150dd8ff394645661fd54951a61361422bd95093fe5e0a5b6f`  
		Last Modified: Tue, 21 Dec 2021 03:34:31 GMT  
		Size: 44.4 MB (44398962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df35a6fcdd7a30ac0a37835fb1e33934c2468b5f30d08368ae3bf49f7bfa461`  
		Last Modified: Tue, 21 Dec 2021 03:34:06 GMT  
		Size: 1.4 MB (1355902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c9336a8d3cba36acf07b1d61a28fd4292af60326e8646e9bf8f69a5ffa9ba8`  
		Last Modified: Wed, 12 Jan 2022 23:01:45 GMT  
		Size: 115.2 MB (115178226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:6eb12e8b0564b926dfaea2f1c2c024c5d1ea0e2cc81f490f308650cdc261105e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193761475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4a4823b4929d867c75cb914eedff1d4662e9724492f8bcd56aa60c8033f899`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 10:42:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 10:42:06 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 10:42:07 GMT
WORKDIR /root
# Wed, 12 Jan 2022 23:28:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727522a568dd0f19904269187584697524c2ca41951cceb1d2c0e2b5cca2b237`  
		Last Modified: Tue, 21 Dec 2021 10:43:15 GMT  
		Size: 49.6 MB (49639004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb72aa07e1e9efbca3d1261e042e1fbe1bb24e1c06e0ec46137338ad38ee1cc`  
		Last Modified: Tue, 21 Dec 2021 10:43:07 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f256e5d107d91c3a6af67b562612d4da625519074a8cecdd6bfe1e712d1043a`  
		Last Modified: Wed, 12 Jan 2022 23:30:04 GMT  
		Size: 116.6 MB (116567394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
