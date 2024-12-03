## `dart:beta-sdk`

```console
$ docker pull dart@sha256:3231dd173296a4f09ce800cd6db8a24e86089ebb7acecefc129a316d802e9be6
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
$ docker pull dart@sha256:7ed9a0143c2a26c33042453c95064ffb0442ce30618628000ef151330aa69803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311931346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc2956049dd172298aa94d28591257a012fd14037fd292563bef6a951e66b31`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 Nov 2024 19:25:25 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead8ae7fa45087b82a04a0ba35e996502d25242be7fe1a0ad119369632719869`  
		Last Modified: Tue, 03 Dec 2024 02:30:20 GMT  
		Size: 54.7 MB (54711933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc95fd66ce7ec08229fb03455e41f2b5684f6603fda66ac9e89161fd0a9f6a9c`  
		Last Modified: Tue, 03 Dec 2024 02:30:18 GMT  
		Size: 1.8 MB (1796913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28054b004a417c0e4247edc9e280c260e0c838d9cb8cda8620b8fc801df6537`  
		Last Modified: Tue, 03 Dec 2024 02:30:24 GMT  
		Size: 227.2 MB (227190888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:aba83a3c243bd2be7f270bd61d08309c61074406257282dbb36915534dc83a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346ac3b5f2ef9e35ea4adc4bf75077de34ad02c05aa916f79c058781cfe7effd`

```dockerfile
```

-	Layers:
	-	`sha256:d101b95198cf6f4317094c6305b93c0d56137179a94af0df88391d6ddeb70a66`  
		Last Modified: Tue, 03 Dec 2024 02:30:18 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:a04a6a402fd2842ba043ecc05e5c90ac6b8d1463579ebc4f474d2ea77a454aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210213772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3994e5acdab12842c98b3673be42e8e589908d72389942eb6e99c8f0be3578`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 Nov 2024 19:25:25 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
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
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee48ebfccf8612e489a704dcaa37efa83ac6c599e5b1901d51fe9719fa5551d6`  
		Last Modified: Tue, 03 Dec 2024 07:43:22 GMT  
		Size: 49.4 MB (49367322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa56c5371336abad086b100e68ad4b0f7f581ee3779293514a5496c8ef72d16f`  
		Last Modified: Tue, 03 Dec 2024 07:43:20 GMT  
		Size: 1.2 MB (1221676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf108133446b0c6ec607d897aa0f88666e252463e9cf1c6b4b074565a5661dd`  
		Last Modified: Tue, 03 Dec 2024 07:44:14 GMT  
		Size: 135.7 MB (135691154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:18d1b41db4efea11795419ba6f8f479d8b366aeb81c3bfe56a7c81ed3036f0f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e4cdab42748ab7fea341dba349b0387fce00a2fd375bf32fa226cecc911a57`

```dockerfile
```

-	Layers:
	-	`sha256:df0eada5cbd1b9d86f2dc146f3cca2d5dff873fc9755b443284a056bce1f3d8b`  
		Last Modified: Tue, 03 Dec 2024 07:44:09 GMT  
		Size: 18.0 KB (18012 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:8f573a661be9ea6ca5b16c62ae4356badc809520e19aff0290c178444b636d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310358346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97d0bf08b9377ebf12a54b98fdd6a10c13c7e2a29cf0abe3984600ce8131372`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 Nov 2024 19:25:25 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b746115c4ad4fc0b69e70a0969769f972133d925a7c115100215eb598e132c`  
		Last Modified: Tue, 03 Dec 2024 05:47:41 GMT  
		Size: 54.5 MB (54478707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89bda1ec4f3c122b646c1435e30dac93ce7f18956bd6b6af84812637b037f92`  
		Last Modified: Tue, 03 Dec 2024 05:47:40 GMT  
		Size: 1.5 MB (1488028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefee6777b55e80fb306c3258f8986d113fcb95134ad7050ae67891cfc519b73`  
		Last Modified: Tue, 03 Dec 2024 05:47:45 GMT  
		Size: 226.3 MB (226332769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4be1abab11d3facfd50be2d40bff66bd487185ae64890e77699a59c5cd88849c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b639ca8e492708bfbdbcf9efe18ec1edf48dcbc585ec8e6f5f374a34b448a0c7`

```dockerfile
```

-	Layers:
	-	`sha256:b7e27ee3e41db61bcd523016d5f30037c40b884f9a5ba3229bc463552de29d44`  
		Last Modified: Tue, 03 Dec 2024 05:47:39 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json
