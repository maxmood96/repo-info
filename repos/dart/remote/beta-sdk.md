## `dart:beta-sdk`

```console
$ docker pull dart@sha256:4c7abb7113c7343223e8d94ec3c96d9ce813fff855c0b44643ff0cb0a24cd5f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:f3dea11af7197fde7a5ebd3c819f5c925a3a5322cc030222ab836c68b94021ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (313017973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062dea51a24fbaaae1e0f3e3992f5ea9e0a02717d950cc8b2819f7db1b56a6e0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410a12dff24c7c1e153368b11ae120799d6e42e9829416389f52e18a0cd6a98b`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 54.9 MB (54905747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887ba69c9a2872567a537db226c706878b04571e5f4be750b3a819ab47ff64a9`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 1.8 MB (1796912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d231c89557df1bfa479abe883fd21f055dd7ed06f85d42bd062212aaae9f991`  
		Last Modified: Tue, 12 Nov 2024 02:39:14 GMT  
		Size: 227.2 MB (227187287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ad2825732d0564cd2f68bee6364c5e22924e7292b382917f0539927e9ba3725a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f02612f6357876164d4af0ce78cfff9959f68c2728a8becad2dcd77fe8e7d4a`

```dockerfile
```

-	Layers:
	-	`sha256:55230a211b499ca64e3b03449d2900f9b32952714f5cdf67565aff7a53cb20c7`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:b55fefa913eac6d194049358fba28c944305b858feeed22c63238a2e4de95a7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211200930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4fe5b34decb961d1e70e5b061869de5474ce2dbd685a33576889076ffb3935`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:41:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:41:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 03:41:29 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 03:41:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 03:41:29 GMT
WORKDIR /root
# Fri, 18 Oct 2024 19:00:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9156a98a1506cc5eaa39325cb70fda804b66d3d8e8dc84710c43864dfed9cf73`  
		Last Modified: Thu, 17 Oct 2024 03:42:30 GMT  
		Size: 49.6 MB (49563698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c941e93242ff85dba1bae0cfe71f142b2855aa56fed6eca21f1f0f80dc5b7a`  
		Last Modified: Thu, 17 Oct 2024 03:42:21 GMT  
		Size: 1.2 MB (1227529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1223942ee36dfb20dc976411e55e67738caf86a1addb1222efd951799472679`  
		Last Modified: Fri, 18 Oct 2024 19:01:27 GMT  
		Size: 135.7 MB (135691506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:86dc7be81abb33732792a7dd8bb8aa9eb643199871f3939e5f29296e5c441de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.7 MB (311661236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578a9e832648fa82a1bb5b547f789a49b83c75576b7b73e1c692a01a3d073449`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30788698cf66de5527ab11fdf6360cfbc0afaa650a7c6760e0b65aee939b94f`  
		Last Modified: Tue, 12 Nov 2024 11:24:43 GMT  
		Size: 54.7 MB (54672293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777e618fc32cc4ac27b04f196b54833b2e942604e13cf31b088c0f7bd901279`  
		Last Modified: Tue, 12 Nov 2024 11:24:41 GMT  
		Size: 1.5 MB (1488031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41075dbe0c552f8c8190f3158065f6e421d6f964452c788ef104b0da777da906`  
		Last Modified: Tue, 12 Nov 2024 11:25:50 GMT  
		Size: 226.3 MB (226343524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c241f0df5694bf7b7e36c7a929aaef16a82f0c7b4b1c24dbbfd2e3ce439a871b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed40ec059cd0a11104875905449c1b2e75e0626e09fce91c141bca35b65ee7f`

```dockerfile
```

-	Layers:
	-	`sha256:d13c8c85bfa0d3c12cb8d2b432ae84f37b33b08e3c97d5b1a48441c19e864812`  
		Last Modified: Tue, 12 Nov 2024 11:25:40 GMT  
		Size: 18.0 KB (18043 bytes)  
		MIME: application/vnd.in-toto+json
