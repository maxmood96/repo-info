## `dart:beta`

```console
$ docker pull dart@sha256:a719c761acc751554a81f71ed78bff3ff3525b7df5e78e95d2a1c6403b663d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:95bbd4a422a74e538d2dbfa72e08051cc57ea0be962b529a70c86a75f59b8d5f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308551806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f10943577cec92a8f5f7c8a4a2c246ae555f84f6d288a8e9d0b5b6dc6e1f1e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:37 GMT
ADD file:d261a6f6921593f1e0b3f472ab1b1822e2c6deb0b369200f0b3370556bfad017 in / 
# Tue, 21 Nov 2023 05:21:37 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:48:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 10:48:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Nov 2023 10:48:15 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Nov 2023 10:48:15 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 10:48:15 GMT
WORKDIR /root
# Thu, 30 Nov 2023 02:38:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2d83ce115bfb588b4ad7d64e31ff7b12578516fc021194104e23fc627f67b32b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c6118c7e0ac718c4e6a4d345ca44ed28343ec5473d9178ce0e31c5159a56d360;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c7703bca5bba8cb17c4469e75a8bf125f97ad62cc9e4b6e4f738cfa9f450eb24;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:1f7ce2fa46ab3942feabee654933948821303a5a821789dddab2d8c3df59e227`  
		Last Modified: Tue, 21 Nov 2023 05:25:58 GMT  
		Size: 29.1 MB (29149908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e6165e1efcd04014f29313052e5aa991a8c21d46e3d8f7f75e379cff4d5a34`  
		Last Modified: Tue, 21 Nov 2023 10:48:53 GMT  
		Size: 54.6 MB (54639926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df8fd9e9f9df68c600f243089b841f066cf605355a7a5559eff4f316ff9e587`  
		Last Modified: Tue, 21 Nov 2023 10:48:46 GMT  
		Size: 1.8 MB (1800648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f716cd34d8003ee6255e0d12e7d1e3fb86a2e0e60791b3c052eb48bae2518917`  
		Last Modified: Thu, 30 Nov 2023 02:39:17 GMT  
		Size: 223.0 MB (222961324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:61080264274cf817c15b5ae879239d63a956619faaf4cb61bc44b88ac607026f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203520772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abdc083f5302ac0911f003b224c19a1f151a31a6a6044e1e2a571bbd6fd96f0a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:57:43 GMT
ADD file:b693944382a95fa47622fde77eb98f0cdeafa40261e7334bd355e00f650b6632 in / 
# Tue, 21 Nov 2023 03:57:43 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 13:55:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 13:55:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Nov 2023 13:55:21 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Nov 2023 13:55:21 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 13:55:21 GMT
WORKDIR /root
# Thu, 30 Nov 2023 00:57:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2d83ce115bfb588b4ad7d64e31ff7b12578516fc021194104e23fc627f67b32b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c6118c7e0ac718c4e6a4d345ca44ed28343ec5473d9178ce0e31c5159a56d360;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c7703bca5bba8cb17c4469e75a8bf125f97ad62cc9e4b6e4f738cfa9f450eb24;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b4ce590529bbcf84326048a22fce76fcfcb5c60af5519debd7935a74c1e9126e`  
		Last Modified: Tue, 21 Nov 2023 04:01:50 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444b7f70f5d85bb0aad85530747df269be0e0344b166741389993499b16dcae1`  
		Last Modified: Tue, 21 Nov 2023 13:55:57 GMT  
		Size: 49.2 MB (49196998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fbb9a22d3262aeff99f80b5978104f76c45c0bc448c95dc625243c0b4e3f32f`  
		Last Modified: Tue, 21 Nov 2023 13:55:50 GMT  
		Size: 1.2 MB (1227218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4868a9c71bf14aa0ff8b5c089da6ebfbeb0abc2a6e6b512fe17ca44636e03972`  
		Last Modified: Thu, 30 Nov 2023 00:58:02 GMT  
		Size: 128.3 MB (128347631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:ac01dbf5fdf5e9e333dc004c21fc69aa6388473ce997333f83e5d06e311c77ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307191870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecbbea46f42293b72434b372280e3143175e6eb39a83f349662bd8f26035061f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:06 GMT
ADD file:869c7d0747a17c53715581a2e862992eb8516c7f45f167821dfa80966a4870d1 in / 
# Tue, 21 Nov 2023 06:27:06 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:27:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 10:27:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Nov 2023 10:27:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Nov 2023 10:27:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 10:27:42 GMT
WORKDIR /root
# Thu, 30 Nov 2023 02:41:36 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=2d83ce115bfb588b4ad7d64e31ff7b12578516fc021194104e23fc627f67b32b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c6118c7e0ac718c4e6a4d345ca44ed28343ec5473d9178ce0e31c5159a56d360;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c7703bca5bba8cb17c4469e75a8bf125f97ad62cc9e4b6e4f738cfa9f450eb24;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2c6d21737d8318aa15c4cc838475029a5efc36c0429e3d8da80d97d0b96d9aaf`  
		Last Modified: Tue, 21 Nov 2023 06:30:30 GMT  
		Size: 29.2 MB (29179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbb99138f7a06fa0f20a243e31157ae2f194ac7776e0fb97854edcbdf7d6381`  
		Last Modified: Tue, 21 Nov 2023 10:28:24 GMT  
		Size: 54.3 MB (54316286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e443916919fb8fb3e4d7942bb9f6f883b08d688e9e5beefc76a177860e2576`  
		Last Modified: Tue, 21 Nov 2023 10:28:18 GMT  
		Size: 1.5 MB (1493569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c028ed82d5d3f477e7a95ce34845953bcf107c5b2e8c7bb7450b206863bcf1ba`  
		Last Modified: Thu, 30 Nov 2023 02:42:17 GMT  
		Size: 222.2 MB (222202738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
