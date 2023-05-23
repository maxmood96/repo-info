## `dart:latest`

```console
$ docker pull dart@sha256:1394a2966192f51085eae53a836c38fc5d7e8df1daf05b793ba0f4ce586b8f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:27eec0959733dc24ec189982ae3d077e510be181abe29c72c0b08e03b3692f2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296597815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a837ef82ead70077fbdbf281c4f1396e2efb0221a4936f3b8d6fb38cec455ba`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:02:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:02:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 23 May 2023 02:02:39 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 23 May 2023 02:02:39 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 02:02:40 GMT
WORKDIR /root
# Tue, 23 May 2023 02:02:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=caab438213bffba5ab704d88155710327f0fc4326594224714271bf823dfdc70;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a36b77fc9eac1b95ca005d262f81af56c359065b18f25d4a4744249772481c4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d05d9052fe8eba57d4838cea5a29577a34988d882ea9610096f137f256409d03;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.0.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3572b44d335a64cd955d4b4f239be22f270eae3cb4aca267178184673f806503`  
		Last Modified: Tue, 23 May 2023 02:03:34 GMT  
		Size: 45.1 MB (45102949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c8976d47ff0430694019e0a77b46eb92804bfcc3a2d3ac81ea6971476f3127`  
		Last Modified: Tue, 23 May 2023 02:03:28 GMT  
		Size: 2.2 MB (2160696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa33627b68d6c306d728d883163e71e7dcc7ec40f527abd2bc263642c573573d`  
		Last Modified: Tue, 23 May 2023 02:03:56 GMT  
		Size: 217.9 MB (217930584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:4ecb8fbd9cef753ac5127cee914992fa630d486c2f043cfe2a8465723109fe6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191265384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55e59a292ffe2bc76ca9b25949bf059e369dd25a8ff7fd83a8cb5d0d5058d86`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:57:55 GMT
ADD file:dbb95e676c7a9806b1883ebcf4259345159caf22ff7194ba7556ea0b1f78099a in / 
# Tue, 23 May 2023 00:57:56 GMT
CMD ["bash"]
# Tue, 23 May 2023 06:32:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 06:32:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 23 May 2023 06:32:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 23 May 2023 06:32:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 06:32:48 GMT
WORKDIR /root
# Tue, 23 May 2023 06:32:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=caab438213bffba5ab704d88155710327f0fc4326594224714271bf823dfdc70;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a36b77fc9eac1b95ca005d262f81af56c359065b18f25d4a4744249772481c4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d05d9052fe8eba57d4838cea5a29577a34988d882ea9610096f137f256409d03;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.0.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a27027e97f260d9b7aac9bae941b44639374700dc4c32cc2e378b189a4ffda88`  
		Last Modified: Tue, 23 May 2023 01:01:46 GMT  
		Size: 26.6 MB (26564635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c657b6b0696f49f6e66ff6f0496b056ebd7e9633d23ad4b260343c03d61dbed6`  
		Last Modified: Tue, 23 May 2023 06:33:34 GMT  
		Size: 41.0 MB (40988340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c024fad8b517f23c3bed43fde74e4a7171250c6f3596db921d6d7cacb0c71792`  
		Last Modified: Tue, 23 May 2023 06:33:28 GMT  
		Size: 1.3 MB (1287723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036e6b1cffaf4c8a8c6c789363f4de07de385a89cb43cb275696d307f880b4c1`  
		Last Modified: Tue, 23 May 2023 06:33:48 GMT  
		Size: 122.4 MB (122424686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:5845dd9c4acf31988517cdaf97e1b600520db609224c92601694804b0f1fb787
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.4 MB (200444999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f5e447997125867e7be36fa3971c65f3357b235e89c36bb496b8a371badf37`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:43:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:43:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 23 May 2023 01:43:43 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 23 May 2023 01:43:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 01:43:44 GMT
WORKDIR /root
# Tue, 23 May 2023 01:43:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=caab438213bffba5ab704d88155710327f0fc4326594224714271bf823dfdc70;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a36b77fc9eac1b95ca005d262f81af56c359065b18f25d4a4744249772481c4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d05d9052fe8eba57d4838cea5a29577a34988d882ea9610096f137f256409d03;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.0.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9834f1e82c8c7a78091fc1d2da8d589129c39bb91a9f424bcca2633901f7d3fe`  
		Last Modified: Tue, 23 May 2023 01:44:25 GMT  
		Size: 45.0 MB (45011120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc4b42a8d93958e89deb953ea286363c4541e1c65e8ea0f3ed34c177a7163b8`  
		Last Modified: Tue, 23 May 2023 01:44:21 GMT  
		Size: 1.6 MB (1560879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf270c9848cb4fc88765bd2280dbf764f19aabb2a7ffd5e0f755209b4490f0e`  
		Last Modified: Tue, 23 May 2023 01:44:33 GMT  
		Size: 123.8 MB (123820253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
