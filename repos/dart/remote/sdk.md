## `dart:sdk`

```console
$ docker pull dart@sha256:693b65a23ec9addfc5ffef57066ed139128ccd180d5d26694002a5df38386771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:b8dd85efd2247de746ec36b432f3fe75304698e634c784905ff71db3c9bf7148
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314055369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60002230c96e424edac54f7e551a344ceae40943ff310904ebb9d91de2d9cb09`
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
# Tue, 14 May 2024 02:50:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6773922a60ce6f3b259dc4877c15f1cd96f325ca48015120014f64171708a7b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=84bd6dc6036993b8d2b41a2012d914a28d9f2e3800fd63ae02d21fb56c467c6f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c3473f681de8717134212c4cabd98ef25ec45c0adddd34e3b0d99431a606bdc9;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:d012a901beacaa056265907731d4bdac6059d8251d2d5452e5de7503d48a73f0`  
		Last Modified: Tue, 14 May 2024 02:51:17 GMT  
		Size: 228.4 MB (228446346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:9de921185c837bcffbe76647f28a3f79fb4bf13e8686ea6d68f7ebc0c4a9cc6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206911583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6162c8cf318befd666e764fb4b2abfb92451b8a7d9f396a17684b6e6ab1975b5`
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
# Tue, 14 May 2024 02:14:36 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6773922a60ce6f3b259dc4877c15f1cd96f325ca48015120014f64171708a7b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=84bd6dc6036993b8d2b41a2012d914a28d9f2e3800fd63ae02d21fb56c467c6f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c3473f681de8717134212c4cabd98ef25ec45c0adddd34e3b0d99431a606bdc9;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:7e0ceb16023b0ca9771a07254eac5e602eed7482109f7ea21e0d699cd108ff2b`  
		Last Modified: Tue, 14 May 2024 02:15:36 GMT  
		Size: 131.8 MB (131806207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3d76821e67b89bef5337936c15756127f25a049365340feaa6692ab62f93a469
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312707451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8db4d1a28ecb4f687aedd4e9b46f0276aad3ad50030cc16dd1f39a9a2c558bf`
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
# Tue, 14 May 2024 07:51:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6773922a60ce6f3b259dc4877c15f1cd96f325ca48015120014f64171708a7b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=84bd6dc6036993b8d2b41a2012d914a28d9f2e3800fd63ae02d21fb56c467c6f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c3473f681de8717134212c4cabd98ef25ec45c0adddd34e3b0d99431a606bdc9;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.3.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:eed957bfdf5d0ea2b80f7bb7659ad271c3bb225dd0847aebe2f770f7f3910100`  
		Last Modified: Tue, 14 May 2024 07:52:58 GMT  
		Size: 227.7 MB (227707584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
