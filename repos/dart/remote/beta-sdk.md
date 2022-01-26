## `dart:beta-sdk`

```console
$ docker pull dart@sha256:d37d6abde2aa98b7c863704467f1601f178e5950b8c1140663d6ceaf76fa901b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:7e05bc2aaa9c1aae4f01673f77b8b5b3cf26612015fdafcbaf61dd57a5bd7a63
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286083236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06abec78d0b6d476f4dbd95d3f8512c08f7136913780a36104d28b9c1462b645`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:35:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:35:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:35:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:35:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:35:56 GMT
WORKDIR /root
# Wed, 26 Jan 2022 02:36:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d2b4ccf63b9160354d63cce1dfd1b47134433047efeb612e2a6373b8d5524bc9;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b3fbb9b5e3c95e2c56d8e0a1d51c841db2908c7afe084842c8e5010a2e45b6f2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=74a9513408c1ab648e93148477f3f59ce609c37289dadd09e83b273369c49fe1;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.16.0-134.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260f85c7c1aebd4382688a5dd10aa11a241660ea1420867bfa423146bb5e7cb1`  
		Last Modified: Wed, 26 Jan 2022 02:37:06 GMT  
		Size: 49.6 MB (49582700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90aea65c283280db5f2c3e5baf6f94dad74c4970a49c4b080c5ac92da97b09df`  
		Last Modified: Wed, 26 Jan 2022 02:36:55 GMT  
		Size: 2.4 MB (2359153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afe93fe40184f720d49ff19ff69cc4cf3386345eb62cba55dbe0058647b9d3b`  
		Last Modified: Wed, 26 Jan 2022 02:38:44 GMT  
		Size: 207.0 MB (206987652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:559b6b31e70e07a80d5f36d99c729ea23d71d186af000f21ad076912e73cd6ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192692248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de9dcb0fa276abf2f71bb70b3526654eae9119198d248870baebabf9c0ebd12`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:43:12 GMT
ADD file:ca8132e20773f7037458cc53fe20a7116f93c21c7479be5a2a1d739495dbe44e in / 
# Wed, 26 Jan 2022 01:43:13 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:25:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:25:00 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:25:01 GMT
WORKDIR /root
# Wed, 26 Jan 2022 02:26:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d2b4ccf63b9160354d63cce1dfd1b47134433047efeb612e2a6373b8d5524bc9;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b3fbb9b5e3c95e2c56d8e0a1d51c841db2908c7afe084842c8e5010a2e45b6f2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=74a9513408c1ab648e93148477f3f59ce609c37289dadd09e83b273369c49fe1;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.16.0-134.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:20cc49690d9072283406c1c11e9b1dc1a247782cc8daa526b375d4a7f1cb6a94`  
		Last Modified: Wed, 26 Jan 2022 01:59:27 GMT  
		Size: 22.8 MB (22754397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9485b7f36107dac4417e8b7c0659296b3ad4a442719e4b2774a85d71ae3f97`  
		Last Modified: Wed, 26 Jan 2022 02:27:46 GMT  
		Size: 44.4 MB (44399462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19668bef3278d9adb593c7b8625c2956fcf32db075c16ae1fa0af31e948fcc0c`  
		Last Modified: Wed, 26 Jan 2022 02:27:25 GMT  
		Size: 1.4 MB (1355911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047f19812d70a0eb4180650cfc6c151fb3a30d83a6774e3803c2b94cd350b3fe`  
		Last Modified: Wed, 26 Jan 2022 02:30:43 GMT  
		Size: 124.2 MB (124182478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:100f408f3a183b1324ba4f3307cfa2f7b9407db3528c1a8a262787d6a7fbf54b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.9 MB (202876518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828b6be055e400eeab084f97744eaf728cffb3d44664848255ef7c72c9eb079c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:56 GMT
ADD file:796bc43a948899ba53bddebf7f613769fe96e8ea3a27eb7143d079c7a166ab01 in / 
# Wed, 26 Jan 2022 01:42:57 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:37:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:37:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:37:43 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:37:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:37:45 GMT
WORKDIR /root
# Wed, 26 Jan 2022 02:38:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d2b4ccf63b9160354d63cce1dfd1b47134433047efeb612e2a6373b8d5524bc9;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b3fbb9b5e3c95e2c56d8e0a1d51c841db2908c7afe084842c8e5010a2e45b6f2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=74a9513408c1ab648e93148477f3f59ce609c37289dadd09e83b273369c49fe1;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.16.0-134.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4c7c9f6f1115fd4f35807a2f6c1375759365a991748aee0111873e55255f150b`  
		Last Modified: Wed, 26 Jan 2022 01:49:55 GMT  
		Size: 25.9 MB (25923216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c695284c12e2e4760a2a37b71f9ed572a621c66646a8fb6336b0dcf6296b13a`  
		Last Modified: Wed, 26 Jan 2022 02:38:51 GMT  
		Size: 49.6 MB (49639076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd03d19014c31feceac42db72787ea78d0fd8a7ffc17bf99ed31807754b1c220`  
		Last Modified: Wed, 26 Jan 2022 02:38:44 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acc6cbcfbb24d2ec3fb11e522c5fb1c5e0396bf3a50241cc2b294bbfdeb4600`  
		Last Modified: Wed, 26 Jan 2022 02:39:57 GMT  
		Size: 125.7 MB (125682298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
