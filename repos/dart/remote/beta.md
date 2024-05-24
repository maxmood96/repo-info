## `dart:beta`

```console
$ docker pull dart@sha256:f182edd660c065a5fb19d85e1c5bc1e8e288814a6039dfb95e4ade7d1e596f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:e10f05d07191121699f01fde81e5a36dacbeb03a53653aa3ffe0a3b53d6e0dc5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322154137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba4e7d9f1199e3cd7e8f7b02f99d552cdaa997165a7a905dff5b80a06f9f96d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:49:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:49:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 14 May 2024 02:49:50 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 May 2024 02:49:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 02:49:51 GMT
WORKDIR /root
# Fri, 24 May 2024 00:36:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d1078d3dc8d69b58b0e9b84e639288206631ae7bf88b13629788e8962029d142;             SDK_ARCH="x64";;         armhf)             DART_SHA256=e04cfe81672dcc126640669f6fc881ba154028e3f2ee22b57b13d0cb54007b9e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=84bc75b0ec3eb5b18690bde364a5a144ccf110f4599c4a2a7d2747d08d9383a8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6473ad03533f00af85f53dba667cc55cac88c26d09fb5367ca61597ca4f87892`  
		Last Modified: Tue, 14 May 2024 02:50:56 GMT  
		Size: 54.7 MB (54657714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c037e904fe4a2fd0e0cff6f7efbb853fd23dcdaf6aa19e53ac853c7308e9fcfb`  
		Last Modified: Tue, 14 May 2024 02:50:48 GMT  
		Size: 1.8 MB (1800898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cdb3e799cf42e9ac12ad46b3d1881f0740e3edf63b8c704719f9d648305341`  
		Last Modified: Fri, 24 May 2024 00:37:20 GMT  
		Size: 236.5 MB (236545114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:73514223381c373eb9d980b81684bdab5d937ce39730598dbc5e083bc0ef3c11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208876205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021fe63a40635129392b42a34972ad9cf0f4ad8ed5db0bf298ccbe3947dc86f5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:14:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:14:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 14 May 2024 02:14:25 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 May 2024 02:14:25 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 02:14:25 GMT
WORKDIR /root
# Fri, 24 May 2024 01:08:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d1078d3dc8d69b58b0e9b84e639288206631ae7bf88b13629788e8962029d142;             SDK_ARCH="x64";;         armhf)             DART_SHA256=e04cfe81672dcc126640669f6fc881ba154028e3f2ee22b57b13d0cb54007b9e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=84bc75b0ec3eb5b18690bde364a5a144ccf110f4599c4a2a7d2747d08d9383a8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb82e079cce59cb431f012a689cb60c01054bb8483580e67dbb899b7ff17881c`  
		Last Modified: Tue, 14 May 2024 02:15:21 GMT  
		Size: 49.1 MB (49137597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4f96d9f56ec4137f3969105775e1f40aaf946e63e896400db4882aaab70bbe`  
		Last Modified: Tue, 14 May 2024 02:15:14 GMT  
		Size: 1.2 MB (1227574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7264ef01945198991f73adf280ccdb9a8c6b2ecded5215b454e1ca162cbdf74a`  
		Last Modified: Fri, 24 May 2024 01:09:07 GMT  
		Size: 133.8 MB (133770829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4bda7531352021cf5570bf79d59caa817a26fa28f5d413c180978a6ab6920545
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.8 MB (320844291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192132220d193681ea89dee00a918b59d1562831014541f888bc312692632cdb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:51:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 07:51:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 14 May 2024 07:51:43 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 May 2024 07:51:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 07:51:43 GMT
WORKDIR /root
# Fri, 24 May 2024 00:41:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d1078d3dc8d69b58b0e9b84e639288206631ae7bf88b13629788e8962029d142;             SDK_ARCH="x64";;         armhf)             DART_SHA256=e04cfe81672dcc126640669f6fc881ba154028e3f2ee22b57b13d0cb54007b9e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=84bc75b0ec3eb5b18690bde364a5a144ccf110f4599c4a2a7d2747d08d9383a8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea6c1ce321fe0889dccf577642f9127a6454cf54e29de5b7b2b2d109fbce885`  
		Last Modified: Tue, 14 May 2024 07:52:40 GMT  
		Size: 54.3 MB (54326056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53765c63261e1d0aeca6398e5bbc7c0a0edc121894d52d2027152ea7227996d8`  
		Last Modified: Tue, 14 May 2024 07:52:35 GMT  
		Size: 1.5 MB (1494308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d909a9ce59c3c6ffc645b0d89bf28a1a457d01f798974f19aab3a6d88a971870`  
		Last Modified: Fri, 24 May 2024 00:41:58 GMT  
		Size: 235.8 MB (235844424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
