## `dart:beta-sdk`

```console
$ docker pull dart@sha256:8f9ccb89e68772720fbedf48baf0f6cc1bf61a6d1fd9962c3a418adbd89bdca0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:5dbf4f6764e9008d213887373d75ecdd5585683dfd3c764e8c9461f51c3da8ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (313021620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965baf44cebebd93d6c2f5a4279a12e291e24e94deb6a3af8c95bedab3321996`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Wed, 13 Nov 2024 19:25:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Nov 2024 19:25:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 13 Nov 2024 19:25:25 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 13 Nov 2024 19:25:25 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Nov 2024 19:25:25 GMT
WORKDIR /root
# Wed, 13 Nov 2024 19:25:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4a97e00d073c74af8b14d45f3251db2f3a3e9718be4be754366b24d50b356ccc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7f21ebfd01e965e3fe2b63c90b440a671e6233c851e8b16f58f52d693844d8c3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=df78b887350eaf0fe4ccda373ce1359461d5e70761d1f79945af028d5dc70e52;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b8e2f64ddf267048ab90067daf039870e80bdea4dba2a06ca46c67cc4ae00a`  
		Last Modified: Thu, 14 Nov 2024 19:06:17 GMT  
		Size: 54.9 MB (54905780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad937d70c5cc0a07a05acc286792f97f61136cf6b3e6920a83e26a4d2492fe44`  
		Last Modified: Thu, 14 Nov 2024 19:06:16 GMT  
		Size: 1.8 MB (1796911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10c63a93e7b1de96db03e969a32095ada97828c3704ec1a40a61102367ff7f6`  
		Last Modified: Thu, 14 Nov 2024 19:06:19 GMT  
		Size: 227.2 MB (227190902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:cea320053f4147722dd498cd9844295ef907c20778b9a66bd1e6006a3d219620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ddcab1f903ecea41fd1e7e49fff00c6dfc6aa9509f1fd53574d3b58728cd4a5`

```dockerfile
```

-	Layers:
	-	`sha256:54add6c3c34cc9a7e6ad0171a80945328aaff913cd4bd8d8b44c082535f4b66f`  
		Last Modified: Thu, 14 Nov 2024 19:06:16 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:b08a2967bf6832f06b771e43f7ef54f7dc6414b9fb2ca3d2764a1ba85f421af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211193726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83bfbd48764dcaacd27db9e3522f0724583dba613e923653239bcaffb591ba22`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Wed, 13 Nov 2024 19:25:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Nov 2024 19:25:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 13 Nov 2024 19:25:25 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 13 Nov 2024 19:25:25 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Nov 2024 19:25:25 GMT
WORKDIR /root
# Wed, 13 Nov 2024 19:25:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4a97e00d073c74af8b14d45f3251db2f3a3e9718be4be754366b24d50b356ccc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7f21ebfd01e965e3fe2b63c90b440a671e6233c851e8b16f58f52d693844d8c3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=df78b887350eaf0fe4ccda373ce1359461d5e70761d1f79945af028d5dc70e52;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09de57ae13fbcb47f749f1466e8424ff54b78d30cc26aa7fa8b6bb510459f11a`  
		Last Modified: Thu, 14 Nov 2024 19:05:46 GMT  
		Size: 49.6 MB (49561516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2537355ee0dcbbe1cd2950f7b518eef85f5c98f687c64289855bc3dada987692`  
		Last Modified: Thu, 14 Nov 2024 19:05:44 GMT  
		Size: 1.2 MB (1221674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20658e45db274d9df530d04ca1cc61919501e38d613f8fc87d52a32271cd1fee`  
		Last Modified: Thu, 14 Nov 2024 19:05:47 GMT  
		Size: 135.7 MB (135691595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0d09c874f41248d7511ef1452a4cf884a9b992e57de75280569a46cefcaec6bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd76881dd57a4b2a71cd1c55a76cca8bc07d200cb776f5c76bccd59035be578b`

```dockerfile
```

-	Layers:
	-	`sha256:48e55596516b0bee7aa7214f984e897148d93417e7f5ef916858db627d4e8ef5`  
		Last Modified: Thu, 14 Nov 2024 19:05:43 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:faa27cbf1d65a536ebeb0b048b1314e4648aedaf956a9a55b63c7114face8e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.7 MB (311650845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450eb6c9fb455b8e3f60aec56b8b0b0f2000ce918af48fdf468a92c9ffee9b00`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Wed, 13 Nov 2024 19:25:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Nov 2024 19:25:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 13 Nov 2024 19:25:25 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 13 Nov 2024 19:25:25 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Nov 2024 19:25:25 GMT
WORKDIR /root
# Wed, 13 Nov 2024 19:25:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4a97e00d073c74af8b14d45f3251db2f3a3e9718be4be754366b24d50b356ccc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7f21ebfd01e965e3fe2b63c90b440a671e6233c851e8b16f58f52d693844d8c3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=df78b887350eaf0fe4ccda373ce1359461d5e70761d1f79945af028d5dc70e52;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8698ab9238689878c2141be5c6c5c3619429c865cc5e2637c20bd217ed27851`  
		Last Modified: Thu, 14 Nov 2024 19:05:51 GMT  
		Size: 54.7 MB (54672420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e35017c647d22e9ab710b2b96757cc08dd187b315acce23b4dbbcf1167be75`  
		Last Modified: Thu, 14 Nov 2024 19:05:50 GMT  
		Size: 1.5 MB (1488031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e45c843c99bd2387fb4118dc90078e055bab2365525790570fb76bc5b9ad2d`  
		Last Modified: Thu, 14 Nov 2024 19:05:55 GMT  
		Size: 226.3 MB (226333006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:38416cfb5ae584f73e250a9837be8fb56a74d97128629ae725f9ea16a333f4e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f199125491acdb1eeec2a980118b456101bf2b20fec8d6b9dda9f32235ee6c5`

```dockerfile
```

-	Layers:
	-	`sha256:258759ebafed90a38c9ae1ad16277bbd03ec95e3c8b1b0346a38bf35b94ca886`  
		Last Modified: Thu, 14 Nov 2024 19:05:49 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json
