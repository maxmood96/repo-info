## `dart:stable-sdk`

```console
$ docker pull dart@sha256:874b39dc7e9068ab1d9a39311875f8c89228c60c07f4705775a1ef977b08e540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:e50914a20b3ab909406ec781948d90b0c8c9909820fbec55ed07d46f92792b47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314025930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9402f21b685991974c990e81f2fde217608256703f2c70bd6b5df4e91fdf1f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:46:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 06:46:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 12 Mar 2024 06:46:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 12 Mar 2024 06:46:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 06:46:59 GMT
WORKDIR /root
# Wed, 27 Mar 2024 19:51:26 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ac7a96f730a632a0960861a6c0bdced033d8c324f6054e6f7dcdea617d77efbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4e0759057c75c1cc3f3036ef4e09fa408742bbb562e6aeebef9c05a848d61d26;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f3da7690e8b238e77fbf2535a0c3336c3ccfb226e431c926f58334910f7ba595;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ace5354dbc86283058a357487ee9c378b9bcc2842de9375634e88a356d98195`  
		Last Modified: Tue, 12 Mar 2024 06:47:54 GMT  
		Size: 54.7 MB (54653679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bec25d09ca9d16965c8552f046592dfab3d4a7d744024fed4b4102e5fb86d5`  
		Last Modified: Tue, 12 Mar 2024 06:47:46 GMT  
		Size: 1.8 MB (1800731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f78a34a81dea8a1a1c2d348ad4e3db727e3b5313f1e8fcc3c07b645dd3d318d`  
		Last Modified: Wed, 27 Mar 2024 19:55:20 GMT  
		Size: 228.4 MB (228447339 bytes)  
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
