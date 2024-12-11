<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.6`](#dart36)
-	[`dart:3.6-sdk`](#dart36-sdk)
-	[`dart:3.6.0`](#dart360)
-	[`dart:3.6.0-sdk`](#dart360-sdk)
-	[`dart:3.7.0-209.1.beta`](#dart370-2091beta)
-	[`dart:3.7.0-209.1.beta-sdk`](#dart370-2091beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:b677df29e01bca3a2d5bdaffe204498834d56a4ed38ff56c0ac6a42d6541b58e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3` - linux; amd64

```console
$ docker pull dart@sha256:89d0c76830a904c54ee083cc3fc309b74d2a093cf1c19094efa39175aa47ccba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311926703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ab72e835098264eaccaf9d36af3f73a3be5f1eaa229064f889f2c59502fc3f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe1c9dc9a62b9b03e26e5f698337db83977923b95cad319712946aeb76dc94c`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 54.7 MB (54711978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af5745f3bebd959ed457c5f7f49c51f08a7bbca8de37cfd105cf2aafcc49bb1`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 1.8 MB (1796915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307d269833d4eb7a10befbc2936a876730b0755a0ab928e7f793ef8b3350db76`  
		Last Modified: Wed, 11 Dec 2024 20:29:34 GMT  
		Size: 227.2 MB (227186198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:1731fb9dbe2205720526f7ec0c456aef42300fd95e467030f58672329f71c8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00936e8602fa8edea3058113a9dfd2bdf31200b47b9e3632718775af423b793`

```dockerfile
```

-	Layers:
	-	`sha256:09193c3748b9697ba9e39e24377e2364e45ef2894dae11b7222f3f68941d4c9b`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:608724c5a50ccafe28198eb03e81b90ace815ba07b9755785fa8e37c2d46a844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210219892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419ec34076f0acf55292fc5bda714f829c3d82da6abe215251af0fccbdcde7dd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec725be604fe98fdc7830e882774c71ae85e4282ccd0eb5f45ad4d90484691e`  
		Last Modified: Wed, 11 Dec 2024 20:31:55 GMT  
		Size: 49.4 MB (49367544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fdb20cdfe82256e6da212f948bfc0b6204d8de0f449e216c6b9afc65cdfa11`  
		Last Modified: Wed, 11 Dec 2024 20:31:54 GMT  
		Size: 1.2 MB (1221678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc76c0501b81aa5a269d87798b170cc8c6411f69f6bfd881f4f3fd7785127c41`  
		Last Modified: Wed, 11 Dec 2024 20:31:58 GMT  
		Size: 135.7 MB (135697050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:660145c166a99a62c92b8d96289353e919693b629bcfd5f78bff30081ab9ddff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8683c04579605303c83c75269e209c639702ea12234ac3d306b85646b077d0`

```dockerfile
```

-	Layers:
	-	`sha256:46a735ef5118294321debc658c3abc00c1984632db49a3a2d95d926ca4df717c`  
		Last Modified: Wed, 11 Dec 2024 20:31:54 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:1d8863b5fa6081006bb5d26b9b29a33c6dbcae0ebf6095011ab229c68c35c35c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310386961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fe4e73074f5d44da2ab84d4e50a3d0d7f9e83d1df6c12c958caf55c1057178`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6757867feefaec653e8deda69d53e16020a2424f9ee2f8815f1031a19dddb3c5`  
		Last Modified: Wed, 11 Dec 2024 20:36:36 GMT  
		Size: 54.5 MB (54478832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f787b3f2c091d822f543fd3294bf3ca088e2876dcea384d170870bef119f6`  
		Last Modified: Wed, 11 Dec 2024 20:36:34 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d77bd7a2ae9ad4ce0e7bfa0635a31081b689507123394d8b35d6b205aa7843`  
		Last Modified: Wed, 11 Dec 2024 20:36:39 GMT  
		Size: 226.4 MB (226361258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:36927f0f0b22c05258d7d4750af7cd02e396a9f22685581174fdd9bbe73c8536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75ff5867af0a09bde531ecc8ffcc18cbe93ef71a4ed4a826b0334b54fb49e1a`

```dockerfile
```

-	Layers:
	-	`sha256:f2d85f90c43e75387b0cbfdcb0959831e067adbd9bf0833eed609e02bcf190ce`  
		Last Modified: Wed, 11 Dec 2024 20:36:34 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:b677df29e01bca3a2d5bdaffe204498834d56a4ed38ff56c0ac6a42d6541b58e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3-sdk` - linux; amd64

```console
$ docker pull dart@sha256:89d0c76830a904c54ee083cc3fc309b74d2a093cf1c19094efa39175aa47ccba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311926703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ab72e835098264eaccaf9d36af3f73a3be5f1eaa229064f889f2c59502fc3f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe1c9dc9a62b9b03e26e5f698337db83977923b95cad319712946aeb76dc94c`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 54.7 MB (54711978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af5745f3bebd959ed457c5f7f49c51f08a7bbca8de37cfd105cf2aafcc49bb1`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 1.8 MB (1796915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307d269833d4eb7a10befbc2936a876730b0755a0ab928e7f793ef8b3350db76`  
		Last Modified: Wed, 11 Dec 2024 20:29:34 GMT  
		Size: 227.2 MB (227186198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1731fb9dbe2205720526f7ec0c456aef42300fd95e467030f58672329f71c8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00936e8602fa8edea3058113a9dfd2bdf31200b47b9e3632718775af423b793`

```dockerfile
```

-	Layers:
	-	`sha256:09193c3748b9697ba9e39e24377e2364e45ef2894dae11b7222f3f68941d4c9b`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:608724c5a50ccafe28198eb03e81b90ace815ba07b9755785fa8e37c2d46a844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210219892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419ec34076f0acf55292fc5bda714f829c3d82da6abe215251af0fccbdcde7dd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec725be604fe98fdc7830e882774c71ae85e4282ccd0eb5f45ad4d90484691e`  
		Last Modified: Wed, 11 Dec 2024 20:31:55 GMT  
		Size: 49.4 MB (49367544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fdb20cdfe82256e6da212f948bfc0b6204d8de0f449e216c6b9afc65cdfa11`  
		Last Modified: Wed, 11 Dec 2024 20:31:54 GMT  
		Size: 1.2 MB (1221678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc76c0501b81aa5a269d87798b170cc8c6411f69f6bfd881f4f3fd7785127c41`  
		Last Modified: Wed, 11 Dec 2024 20:31:58 GMT  
		Size: 135.7 MB (135697050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:660145c166a99a62c92b8d96289353e919693b629bcfd5f78bff30081ab9ddff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8683c04579605303c83c75269e209c639702ea12234ac3d306b85646b077d0`

```dockerfile
```

-	Layers:
	-	`sha256:46a735ef5118294321debc658c3abc00c1984632db49a3a2d95d926ca4df717c`  
		Last Modified: Wed, 11 Dec 2024 20:31:54 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:1d8863b5fa6081006bb5d26b9b29a33c6dbcae0ebf6095011ab229c68c35c35c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310386961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fe4e73074f5d44da2ab84d4e50a3d0d7f9e83d1df6c12c958caf55c1057178`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6757867feefaec653e8deda69d53e16020a2424f9ee2f8815f1031a19dddb3c5`  
		Last Modified: Wed, 11 Dec 2024 20:36:36 GMT  
		Size: 54.5 MB (54478832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f787b3f2c091d822f543fd3294bf3ca088e2876dcea384d170870bef119f6`  
		Last Modified: Wed, 11 Dec 2024 20:36:34 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d77bd7a2ae9ad4ce0e7bfa0635a31081b689507123394d8b35d6b205aa7843`  
		Last Modified: Wed, 11 Dec 2024 20:36:39 GMT  
		Size: 226.4 MB (226361258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:36927f0f0b22c05258d7d4750af7cd02e396a9f22685581174fdd9bbe73c8536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75ff5867af0a09bde531ecc8ffcc18cbe93ef71a4ed4a826b0334b54fb49e1a`

```dockerfile
```

-	Layers:
	-	`sha256:f2d85f90c43e75387b0cbfdcb0959831e067adbd9bf0833eed609e02bcf190ce`  
		Last Modified: Wed, 11 Dec 2024 20:36:34 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.6`

```console
$ docker pull dart@sha256:b677df29e01bca3a2d5bdaffe204498834d56a4ed38ff56c0ac6a42d6541b58e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.6` - linux; amd64

```console
$ docker pull dart@sha256:89d0c76830a904c54ee083cc3fc309b74d2a093cf1c19094efa39175aa47ccba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311926703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ab72e835098264eaccaf9d36af3f73a3be5f1eaa229064f889f2c59502fc3f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe1c9dc9a62b9b03e26e5f698337db83977923b95cad319712946aeb76dc94c`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 54.7 MB (54711978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af5745f3bebd959ed457c5f7f49c51f08a7bbca8de37cfd105cf2aafcc49bb1`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 1.8 MB (1796915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307d269833d4eb7a10befbc2936a876730b0755a0ab928e7f793ef8b3350db76`  
		Last Modified: Wed, 11 Dec 2024 20:29:34 GMT  
		Size: 227.2 MB (227186198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6` - unknown; unknown

```console
$ docker pull dart@sha256:1731fb9dbe2205720526f7ec0c456aef42300fd95e467030f58672329f71c8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00936e8602fa8edea3058113a9dfd2bdf31200b47b9e3632718775af423b793`

```dockerfile
```

-	Layers:
	-	`sha256:09193c3748b9697ba9e39e24377e2364e45ef2894dae11b7222f3f68941d4c9b`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.6` - linux; arm variant v7

```console
$ docker pull dart@sha256:608724c5a50ccafe28198eb03e81b90ace815ba07b9755785fa8e37c2d46a844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210219892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419ec34076f0acf55292fc5bda714f829c3d82da6abe215251af0fccbdcde7dd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec725be604fe98fdc7830e882774c71ae85e4282ccd0eb5f45ad4d90484691e`  
		Last Modified: Wed, 11 Dec 2024 20:31:55 GMT  
		Size: 49.4 MB (49367544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fdb20cdfe82256e6da212f948bfc0b6204d8de0f449e216c6b9afc65cdfa11`  
		Last Modified: Wed, 11 Dec 2024 20:31:54 GMT  
		Size: 1.2 MB (1221678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc76c0501b81aa5a269d87798b170cc8c6411f69f6bfd881f4f3fd7785127c41`  
		Last Modified: Wed, 11 Dec 2024 20:31:58 GMT  
		Size: 135.7 MB (135697050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6` - unknown; unknown

```console
$ docker pull dart@sha256:660145c166a99a62c92b8d96289353e919693b629bcfd5f78bff30081ab9ddff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8683c04579605303c83c75269e209c639702ea12234ac3d306b85646b077d0`

```dockerfile
```

-	Layers:
	-	`sha256:46a735ef5118294321debc658c3abc00c1984632db49a3a2d95d926ca4df717c`  
		Last Modified: Wed, 11 Dec 2024 20:31:54 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.6` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:1d8863b5fa6081006bb5d26b9b29a33c6dbcae0ebf6095011ab229c68c35c35c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310386961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fe4e73074f5d44da2ab84d4e50a3d0d7f9e83d1df6c12c958caf55c1057178`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6757867feefaec653e8deda69d53e16020a2424f9ee2f8815f1031a19dddb3c5`  
		Last Modified: Wed, 11 Dec 2024 20:36:36 GMT  
		Size: 54.5 MB (54478832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f787b3f2c091d822f543fd3294bf3ca088e2876dcea384d170870bef119f6`  
		Last Modified: Wed, 11 Dec 2024 20:36:34 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d77bd7a2ae9ad4ce0e7bfa0635a31081b689507123394d8b35d6b205aa7843`  
		Last Modified: Wed, 11 Dec 2024 20:36:39 GMT  
		Size: 226.4 MB (226361258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6` - unknown; unknown

```console
$ docker pull dart@sha256:36927f0f0b22c05258d7d4750af7cd02e396a9f22685581174fdd9bbe73c8536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75ff5867af0a09bde531ecc8ffcc18cbe93ef71a4ed4a826b0334b54fb49e1a`

```dockerfile
```

-	Layers:
	-	`sha256:f2d85f90c43e75387b0cbfdcb0959831e067adbd9bf0833eed609e02bcf190ce`  
		Last Modified: Wed, 11 Dec 2024 20:36:34 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.6-sdk`

```console
$ docker pull dart@sha256:b677df29e01bca3a2d5bdaffe204498834d56a4ed38ff56c0ac6a42d6541b58e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.6-sdk` - linux; amd64

```console
$ docker pull dart@sha256:89d0c76830a904c54ee083cc3fc309b74d2a093cf1c19094efa39175aa47ccba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311926703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ab72e835098264eaccaf9d36af3f73a3be5f1eaa229064f889f2c59502fc3f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe1c9dc9a62b9b03e26e5f698337db83977923b95cad319712946aeb76dc94c`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 54.7 MB (54711978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af5745f3bebd959ed457c5f7f49c51f08a7bbca8de37cfd105cf2aafcc49bb1`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 1.8 MB (1796915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307d269833d4eb7a10befbc2936a876730b0755a0ab928e7f793ef8b3350db76`  
		Last Modified: Wed, 11 Dec 2024 20:29:34 GMT  
		Size: 227.2 MB (227186198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1731fb9dbe2205720526f7ec0c456aef42300fd95e467030f58672329f71c8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00936e8602fa8edea3058113a9dfd2bdf31200b47b9e3632718775af423b793`

```dockerfile
```

-	Layers:
	-	`sha256:09193c3748b9697ba9e39e24377e2364e45ef2894dae11b7222f3f68941d4c9b`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.6-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:608724c5a50ccafe28198eb03e81b90ace815ba07b9755785fa8e37c2d46a844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210219892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419ec34076f0acf55292fc5bda714f829c3d82da6abe215251af0fccbdcde7dd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec725be604fe98fdc7830e882774c71ae85e4282ccd0eb5f45ad4d90484691e`  
		Last Modified: Wed, 11 Dec 2024 20:31:55 GMT  
		Size: 49.4 MB (49367544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fdb20cdfe82256e6da212f948bfc0b6204d8de0f449e216c6b9afc65cdfa11`  
		Last Modified: Wed, 11 Dec 2024 20:31:54 GMT  
		Size: 1.2 MB (1221678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc76c0501b81aa5a269d87798b170cc8c6411f69f6bfd881f4f3fd7785127c41`  
		Last Modified: Wed, 11 Dec 2024 20:31:58 GMT  
		Size: 135.7 MB (135697050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:660145c166a99a62c92b8d96289353e919693b629bcfd5f78bff30081ab9ddff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8683c04579605303c83c75269e209c639702ea12234ac3d306b85646b077d0`

```dockerfile
```

-	Layers:
	-	`sha256:46a735ef5118294321debc658c3abc00c1984632db49a3a2d95d926ca4df717c`  
		Last Modified: Wed, 11 Dec 2024 20:31:54 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.6-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:1d8863b5fa6081006bb5d26b9b29a33c6dbcae0ebf6095011ab229c68c35c35c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310386961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fe4e73074f5d44da2ab84d4e50a3d0d7f9e83d1df6c12c958caf55c1057178`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6757867feefaec653e8deda69d53e16020a2424f9ee2f8815f1031a19dddb3c5`  
		Last Modified: Wed, 11 Dec 2024 20:36:36 GMT  
		Size: 54.5 MB (54478832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f787b3f2c091d822f543fd3294bf3ca088e2876dcea384d170870bef119f6`  
		Last Modified: Wed, 11 Dec 2024 20:36:34 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d77bd7a2ae9ad4ce0e7bfa0635a31081b689507123394d8b35d6b205aa7843`  
		Last Modified: Wed, 11 Dec 2024 20:36:39 GMT  
		Size: 226.4 MB (226361258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:36927f0f0b22c05258d7d4750af7cd02e396a9f22685581174fdd9bbe73c8536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75ff5867af0a09bde531ecc8ffcc18cbe93ef71a4ed4a826b0334b54fb49e1a`

```dockerfile
```

-	Layers:
	-	`sha256:f2d85f90c43e75387b0cbfdcb0959831e067adbd9bf0833eed609e02bcf190ce`  
		Last Modified: Wed, 11 Dec 2024 20:36:34 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.6.0`

```console
$ docker pull dart@sha256:b677df29e01bca3a2d5bdaffe204498834d56a4ed38ff56c0ac6a42d6541b58e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.6.0` - linux; amd64

```console
$ docker pull dart@sha256:89d0c76830a904c54ee083cc3fc309b74d2a093cf1c19094efa39175aa47ccba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311926703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ab72e835098264eaccaf9d36af3f73a3be5f1eaa229064f889f2c59502fc3f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe1c9dc9a62b9b03e26e5f698337db83977923b95cad319712946aeb76dc94c`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 54.7 MB (54711978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af5745f3bebd959ed457c5f7f49c51f08a7bbca8de37cfd105cf2aafcc49bb1`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 1.8 MB (1796915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307d269833d4eb7a10befbc2936a876730b0755a0ab928e7f793ef8b3350db76`  
		Last Modified: Wed, 11 Dec 2024 20:29:34 GMT  
		Size: 227.2 MB (227186198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6.0` - unknown; unknown

```console
$ docker pull dart@sha256:1731fb9dbe2205720526f7ec0c456aef42300fd95e467030f58672329f71c8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00936e8602fa8edea3058113a9dfd2bdf31200b47b9e3632718775af423b793`

```dockerfile
```

-	Layers:
	-	`sha256:09193c3748b9697ba9e39e24377e2364e45ef2894dae11b7222f3f68941d4c9b`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.6.0` - linux; arm variant v7

```console
$ docker pull dart@sha256:608724c5a50ccafe28198eb03e81b90ace815ba07b9755785fa8e37c2d46a844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210219892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419ec34076f0acf55292fc5bda714f829c3d82da6abe215251af0fccbdcde7dd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec725be604fe98fdc7830e882774c71ae85e4282ccd0eb5f45ad4d90484691e`  
		Last Modified: Wed, 11 Dec 2024 20:31:55 GMT  
		Size: 49.4 MB (49367544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fdb20cdfe82256e6da212f948bfc0b6204d8de0f449e216c6b9afc65cdfa11`  
		Last Modified: Wed, 11 Dec 2024 20:31:54 GMT  
		Size: 1.2 MB (1221678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc76c0501b81aa5a269d87798b170cc8c6411f69f6bfd881f4f3fd7785127c41`  
		Last Modified: Wed, 11 Dec 2024 20:31:58 GMT  
		Size: 135.7 MB (135697050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6.0` - unknown; unknown

```console
$ docker pull dart@sha256:660145c166a99a62c92b8d96289353e919693b629bcfd5f78bff30081ab9ddff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8683c04579605303c83c75269e209c639702ea12234ac3d306b85646b077d0`

```dockerfile
```

-	Layers:
	-	`sha256:46a735ef5118294321debc658c3abc00c1984632db49a3a2d95d926ca4df717c`  
		Last Modified: Wed, 11 Dec 2024 20:31:54 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.6.0` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:1d8863b5fa6081006bb5d26b9b29a33c6dbcae0ebf6095011ab229c68c35c35c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310386961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fe4e73074f5d44da2ab84d4e50a3d0d7f9e83d1df6c12c958caf55c1057178`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6757867feefaec653e8deda69d53e16020a2424f9ee2f8815f1031a19dddb3c5`  
		Last Modified: Wed, 11 Dec 2024 20:36:36 GMT  
		Size: 54.5 MB (54478832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f787b3f2c091d822f543fd3294bf3ca088e2876dcea384d170870bef119f6`  
		Last Modified: Wed, 11 Dec 2024 20:36:34 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d77bd7a2ae9ad4ce0e7bfa0635a31081b689507123394d8b35d6b205aa7843`  
		Last Modified: Wed, 11 Dec 2024 20:36:39 GMT  
		Size: 226.4 MB (226361258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6.0` - unknown; unknown

```console
$ docker pull dart@sha256:36927f0f0b22c05258d7d4750af7cd02e396a9f22685581174fdd9bbe73c8536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75ff5867af0a09bde531ecc8ffcc18cbe93ef71a4ed4a826b0334b54fb49e1a`

```dockerfile
```

-	Layers:
	-	`sha256:f2d85f90c43e75387b0cbfdcb0959831e067adbd9bf0833eed609e02bcf190ce`  
		Last Modified: Wed, 11 Dec 2024 20:36:34 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.6.0-sdk`

```console
$ docker pull dart@sha256:b677df29e01bca3a2d5bdaffe204498834d56a4ed38ff56c0ac6a42d6541b58e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.6.0-sdk` - linux; amd64

```console
$ docker pull dart@sha256:89d0c76830a904c54ee083cc3fc309b74d2a093cf1c19094efa39175aa47ccba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311926703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ab72e835098264eaccaf9d36af3f73a3be5f1eaa229064f889f2c59502fc3f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe1c9dc9a62b9b03e26e5f698337db83977923b95cad319712946aeb76dc94c`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 54.7 MB (54711978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af5745f3bebd959ed457c5f7f49c51f08a7bbca8de37cfd105cf2aafcc49bb1`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 1.8 MB (1796915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307d269833d4eb7a10befbc2936a876730b0755a0ab928e7f793ef8b3350db76`  
		Last Modified: Wed, 11 Dec 2024 20:29:34 GMT  
		Size: 227.2 MB (227186198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6.0-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1731fb9dbe2205720526f7ec0c456aef42300fd95e467030f58672329f71c8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00936e8602fa8edea3058113a9dfd2bdf31200b47b9e3632718775af423b793`

```dockerfile
```

-	Layers:
	-	`sha256:09193c3748b9697ba9e39e24377e2364e45ef2894dae11b7222f3f68941d4c9b`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.6.0-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:608724c5a50ccafe28198eb03e81b90ace815ba07b9755785fa8e37c2d46a844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210219892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419ec34076f0acf55292fc5bda714f829c3d82da6abe215251af0fccbdcde7dd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec725be604fe98fdc7830e882774c71ae85e4282ccd0eb5f45ad4d90484691e`  
		Last Modified: Wed, 11 Dec 2024 20:31:55 GMT  
		Size: 49.4 MB (49367544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fdb20cdfe82256e6da212f948bfc0b6204d8de0f449e216c6b9afc65cdfa11`  
		Last Modified: Wed, 11 Dec 2024 20:31:54 GMT  
		Size: 1.2 MB (1221678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc76c0501b81aa5a269d87798b170cc8c6411f69f6bfd881f4f3fd7785127c41`  
		Last Modified: Wed, 11 Dec 2024 20:31:58 GMT  
		Size: 135.7 MB (135697050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6.0-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:660145c166a99a62c92b8d96289353e919693b629bcfd5f78bff30081ab9ddff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8683c04579605303c83c75269e209c639702ea12234ac3d306b85646b077d0`

```dockerfile
```

-	Layers:
	-	`sha256:46a735ef5118294321debc658c3abc00c1984632db49a3a2d95d926ca4df717c`  
		Last Modified: Wed, 11 Dec 2024 20:31:54 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.6.0-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:1d8863b5fa6081006bb5d26b9b29a33c6dbcae0ebf6095011ab229c68c35c35c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310386961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fe4e73074f5d44da2ab84d4e50a3d0d7f9e83d1df6c12c958caf55c1057178`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6757867feefaec653e8deda69d53e16020a2424f9ee2f8815f1031a19dddb3c5`  
		Last Modified: Wed, 11 Dec 2024 20:36:36 GMT  
		Size: 54.5 MB (54478832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f787b3f2c091d822f543fd3294bf3ca088e2876dcea384d170870bef119f6`  
		Last Modified: Wed, 11 Dec 2024 20:36:34 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d77bd7a2ae9ad4ce0e7bfa0635a31081b689507123394d8b35d6b205aa7843`  
		Last Modified: Wed, 11 Dec 2024 20:36:39 GMT  
		Size: 226.4 MB (226361258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6.0-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:36927f0f0b22c05258d7d4750af7cd02e396a9f22685581174fdd9bbe73c8536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75ff5867af0a09bde531ecc8ffcc18cbe93ef71a4ed4a826b0334b54fb49e1a`

```dockerfile
```

-	Layers:
	-	`sha256:f2d85f90c43e75387b0cbfdcb0959831e067adbd9bf0833eed609e02bcf190ce`  
		Last Modified: Wed, 11 Dec 2024 20:36:34 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.7.0-209.1.beta`

```console
$ docker pull dart@sha256:4d9e8d73a27a2945f65005b00ea6e25d755dd1405b8a8f882fa296b4f85238f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.7.0-209.1.beta` - linux; amd64

```console
$ docker pull dart@sha256:53255de7d7f902c438aadecf1c3199a1affb8ae58d4d646a4575b541c3bee9ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302253145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e9152a48447b4d6bd3b3965eea8b4c65dcf545aa21e6c418cb1ada907f844f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4fdc270a09982dea04f2e7ea285e8e0356f2d0847cb2ee5c774bcb70b54111`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 54.7 MB (54712053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4378ab2daf5f0b664a0626873b524806e55eae6344628c37c8306eadcef69484`  
		Last Modified: Wed, 11 Dec 2024 20:29:30 GMT  
		Size: 1.8 MB (1796905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ceadeaffe8cdc93886526f59fdb4d2b8402f528c3c0b339c83daa66593e8737`  
		Last Modified: Wed, 11 Dec 2024 20:29:34 GMT  
		Size: 217.5 MB (217512575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.0-209.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:a38de2cd5d09832cd1cf6ce4a64cc20ed72f4220c218901cfc1bb148d17f72af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f263394f57357795be998cdf4a18fdb41376b02ff1551b2e0b3bf19d07c9955e`

```dockerfile
```

-	Layers:
	-	`sha256:6422fd37ebcde54460de4f5eda898ed32cfde14e49d2ac7466e659da6a8db5fe`  
		Last Modified: Wed, 11 Dec 2024 20:29:30 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7.0-209.1.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:f5b7caa30ebdba03d382a7af5f1d0e20da0f74216141bff6b1662a2f1638cd09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224753449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f039b787716e2fb03bdefbf41988f7d6d1b33d593f4692dbee1a6f187747be62`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec725be604fe98fdc7830e882774c71ae85e4282ccd0eb5f45ad4d90484691e`  
		Last Modified: Wed, 11 Dec 2024 20:31:55 GMT  
		Size: 49.4 MB (49367544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fdb20cdfe82256e6da212f948bfc0b6204d8de0f449e216c6b9afc65cdfa11`  
		Last Modified: Wed, 11 Dec 2024 20:31:54 GMT  
		Size: 1.2 MB (1221678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8edf925ff8cff435a926ee74aeb9053ceb1005b17220224e192fd48aa34b8d`  
		Last Modified: Wed, 11 Dec 2024 20:32:55 GMT  
		Size: 150.2 MB (150230607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.0-209.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:66a8ad0443624d2f28a380089001c09579106128d7b1338564ad458ab8c07de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a26665b8684b2c9af56906e7c5646e2582d44726ef343bafb8e4360282ce106`

```dockerfile
```

-	Layers:
	-	`sha256:73ca1098fde4ca6b5cd9a735f77a0aeff5c6966d555450e54329692bc42047f3`  
		Last Modified: Wed, 11 Dec 2024 20:32:48 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7.0-209.1.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f92323307d136fb897c38a14981d2507d11d44b4cc0df6dd01e71ca0805e144b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300891299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1428f2a674ec67789edcafc2534a444a21feebf62427ad9073b72695e3a1ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6757867feefaec653e8deda69d53e16020a2424f9ee2f8815f1031a19dddb3c5`  
		Last Modified: Wed, 11 Dec 2024 20:36:36 GMT  
		Size: 54.5 MB (54478832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f787b3f2c091d822f543fd3294bf3ca088e2876dcea384d170870bef119f6`  
		Last Modified: Wed, 11 Dec 2024 20:36:34 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7162579a043fe7c05532fec8d722108b57e9ceaaeb439818c5e098ceeaa677`  
		Last Modified: Wed, 11 Dec 2024 20:37:30 GMT  
		Size: 216.9 MB (216865596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.0-209.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:c2233f8529b1c2577af9165d99da0eeec282c6db13c62cf57cfef7f3a34959c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18d9648f5909cecd8aaeb7087dbeff8e01c325803f9be97c44cce340fcb6425`

```dockerfile
```

-	Layers:
	-	`sha256:923564f8f57ebc6559a3f01ada4d54463906c0076fdfa059450e25a3db526395`  
		Last Modified: Wed, 11 Dec 2024 20:37:25 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.7.0-209.1.beta-sdk`

```console
$ docker pull dart@sha256:4d9e8d73a27a2945f65005b00ea6e25d755dd1405b8a8f882fa296b4f85238f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.7.0-209.1.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:53255de7d7f902c438aadecf1c3199a1affb8ae58d4d646a4575b541c3bee9ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302253145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e9152a48447b4d6bd3b3965eea8b4c65dcf545aa21e6c418cb1ada907f844f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4fdc270a09982dea04f2e7ea285e8e0356f2d0847cb2ee5c774bcb70b54111`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 54.7 MB (54712053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4378ab2daf5f0b664a0626873b524806e55eae6344628c37c8306eadcef69484`  
		Last Modified: Wed, 11 Dec 2024 20:29:30 GMT  
		Size: 1.8 MB (1796905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ceadeaffe8cdc93886526f59fdb4d2b8402f528c3c0b339c83daa66593e8737`  
		Last Modified: Wed, 11 Dec 2024 20:29:34 GMT  
		Size: 217.5 MB (217512575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.0-209.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a38de2cd5d09832cd1cf6ce4a64cc20ed72f4220c218901cfc1bb148d17f72af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f263394f57357795be998cdf4a18fdb41376b02ff1551b2e0b3bf19d07c9955e`

```dockerfile
```

-	Layers:
	-	`sha256:6422fd37ebcde54460de4f5eda898ed32cfde14e49d2ac7466e659da6a8db5fe`  
		Last Modified: Wed, 11 Dec 2024 20:29:30 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7.0-209.1.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:f5b7caa30ebdba03d382a7af5f1d0e20da0f74216141bff6b1662a2f1638cd09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224753449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f039b787716e2fb03bdefbf41988f7d6d1b33d593f4692dbee1a6f187747be62`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec725be604fe98fdc7830e882774c71ae85e4282ccd0eb5f45ad4d90484691e`  
		Last Modified: Wed, 11 Dec 2024 20:31:55 GMT  
		Size: 49.4 MB (49367544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fdb20cdfe82256e6da212f948bfc0b6204d8de0f449e216c6b9afc65cdfa11`  
		Last Modified: Wed, 11 Dec 2024 20:31:54 GMT  
		Size: 1.2 MB (1221678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8edf925ff8cff435a926ee74aeb9053ceb1005b17220224e192fd48aa34b8d`  
		Last Modified: Wed, 11 Dec 2024 20:32:55 GMT  
		Size: 150.2 MB (150230607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.0-209.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:66a8ad0443624d2f28a380089001c09579106128d7b1338564ad458ab8c07de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a26665b8684b2c9af56906e7c5646e2582d44726ef343bafb8e4360282ce106`

```dockerfile
```

-	Layers:
	-	`sha256:73ca1098fde4ca6b5cd9a735f77a0aeff5c6966d555450e54329692bc42047f3`  
		Last Modified: Wed, 11 Dec 2024 20:32:48 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7.0-209.1.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f92323307d136fb897c38a14981d2507d11d44b4cc0df6dd01e71ca0805e144b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300891299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1428f2a674ec67789edcafc2534a444a21feebf62427ad9073b72695e3a1ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6757867feefaec653e8deda69d53e16020a2424f9ee2f8815f1031a19dddb3c5`  
		Last Modified: Wed, 11 Dec 2024 20:36:36 GMT  
		Size: 54.5 MB (54478832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f787b3f2c091d822f543fd3294bf3ca088e2876dcea384d170870bef119f6`  
		Last Modified: Wed, 11 Dec 2024 20:36:34 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7162579a043fe7c05532fec8d722108b57e9ceaaeb439818c5e098ceeaa677`  
		Last Modified: Wed, 11 Dec 2024 20:37:30 GMT  
		Size: 216.9 MB (216865596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.0-209.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c2233f8529b1c2577af9165d99da0eeec282c6db13c62cf57cfef7f3a34959c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18d9648f5909cecd8aaeb7087dbeff8e01c325803f9be97c44cce340fcb6425`

```dockerfile
```

-	Layers:
	-	`sha256:923564f8f57ebc6559a3f01ada4d54463906c0076fdfa059450e25a3db526395`  
		Last Modified: Wed, 11 Dec 2024 20:37:25 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:4d9e8d73a27a2945f65005b00ea6e25d755dd1405b8a8f882fa296b4f85238f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:53255de7d7f902c438aadecf1c3199a1affb8ae58d4d646a4575b541c3bee9ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302253145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e9152a48447b4d6bd3b3965eea8b4c65dcf545aa21e6c418cb1ada907f844f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4fdc270a09982dea04f2e7ea285e8e0356f2d0847cb2ee5c774bcb70b54111`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 54.7 MB (54712053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4378ab2daf5f0b664a0626873b524806e55eae6344628c37c8306eadcef69484`  
		Last Modified: Wed, 11 Dec 2024 20:29:30 GMT  
		Size: 1.8 MB (1796905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ceadeaffe8cdc93886526f59fdb4d2b8402f528c3c0b339c83daa66593e8737`  
		Last Modified: Wed, 11 Dec 2024 20:29:34 GMT  
		Size: 217.5 MB (217512575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:a38de2cd5d09832cd1cf6ce4a64cc20ed72f4220c218901cfc1bb148d17f72af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f263394f57357795be998cdf4a18fdb41376b02ff1551b2e0b3bf19d07c9955e`

```dockerfile
```

-	Layers:
	-	`sha256:6422fd37ebcde54460de4f5eda898ed32cfde14e49d2ac7466e659da6a8db5fe`  
		Last Modified: Wed, 11 Dec 2024 20:29:30 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:f5b7caa30ebdba03d382a7af5f1d0e20da0f74216141bff6b1662a2f1638cd09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224753449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f039b787716e2fb03bdefbf41988f7d6d1b33d593f4692dbee1a6f187747be62`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec725be604fe98fdc7830e882774c71ae85e4282ccd0eb5f45ad4d90484691e`  
		Last Modified: Wed, 11 Dec 2024 20:31:55 GMT  
		Size: 49.4 MB (49367544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fdb20cdfe82256e6da212f948bfc0b6204d8de0f449e216c6b9afc65cdfa11`  
		Last Modified: Wed, 11 Dec 2024 20:31:54 GMT  
		Size: 1.2 MB (1221678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8edf925ff8cff435a926ee74aeb9053ceb1005b17220224e192fd48aa34b8d`  
		Last Modified: Wed, 11 Dec 2024 20:32:55 GMT  
		Size: 150.2 MB (150230607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:66a8ad0443624d2f28a380089001c09579106128d7b1338564ad458ab8c07de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a26665b8684b2c9af56906e7c5646e2582d44726ef343bafb8e4360282ce106`

```dockerfile
```

-	Layers:
	-	`sha256:73ca1098fde4ca6b5cd9a735f77a0aeff5c6966d555450e54329692bc42047f3`  
		Last Modified: Wed, 11 Dec 2024 20:32:48 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f92323307d136fb897c38a14981d2507d11d44b4cc0df6dd01e71ca0805e144b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300891299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1428f2a674ec67789edcafc2534a444a21feebf62427ad9073b72695e3a1ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6757867feefaec653e8deda69d53e16020a2424f9ee2f8815f1031a19dddb3c5`  
		Last Modified: Wed, 11 Dec 2024 20:36:36 GMT  
		Size: 54.5 MB (54478832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f787b3f2c091d822f543fd3294bf3ca088e2876dcea384d170870bef119f6`  
		Last Modified: Wed, 11 Dec 2024 20:36:34 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7162579a043fe7c05532fec8d722108b57e9ceaaeb439818c5e098ceeaa677`  
		Last Modified: Wed, 11 Dec 2024 20:37:30 GMT  
		Size: 216.9 MB (216865596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:c2233f8529b1c2577af9165d99da0eeec282c6db13c62cf57cfef7f3a34959c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18d9648f5909cecd8aaeb7087dbeff8e01c325803f9be97c44cce340fcb6425`

```dockerfile
```

-	Layers:
	-	`sha256:923564f8f57ebc6559a3f01ada4d54463906c0076fdfa059450e25a3db526395`  
		Last Modified: Wed, 11 Dec 2024 20:37:25 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:4d9e8d73a27a2945f65005b00ea6e25d755dd1405b8a8f882fa296b4f85238f3
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
$ docker pull dart@sha256:53255de7d7f902c438aadecf1c3199a1affb8ae58d4d646a4575b541c3bee9ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302253145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e9152a48447b4d6bd3b3965eea8b4c65dcf545aa21e6c418cb1ada907f844f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4fdc270a09982dea04f2e7ea285e8e0356f2d0847cb2ee5c774bcb70b54111`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 54.7 MB (54712053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4378ab2daf5f0b664a0626873b524806e55eae6344628c37c8306eadcef69484`  
		Last Modified: Wed, 11 Dec 2024 20:29:30 GMT  
		Size: 1.8 MB (1796905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ceadeaffe8cdc93886526f59fdb4d2b8402f528c3c0b339c83daa66593e8737`  
		Last Modified: Wed, 11 Dec 2024 20:29:34 GMT  
		Size: 217.5 MB (217512575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a38de2cd5d09832cd1cf6ce4a64cc20ed72f4220c218901cfc1bb148d17f72af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f263394f57357795be998cdf4a18fdb41376b02ff1551b2e0b3bf19d07c9955e`

```dockerfile
```

-	Layers:
	-	`sha256:6422fd37ebcde54460de4f5eda898ed32cfde14e49d2ac7466e659da6a8db5fe`  
		Last Modified: Wed, 11 Dec 2024 20:29:30 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:f5b7caa30ebdba03d382a7af5f1d0e20da0f74216141bff6b1662a2f1638cd09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224753449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f039b787716e2fb03bdefbf41988f7d6d1b33d593f4692dbee1a6f187747be62`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec725be604fe98fdc7830e882774c71ae85e4282ccd0eb5f45ad4d90484691e`  
		Last Modified: Wed, 11 Dec 2024 20:31:55 GMT  
		Size: 49.4 MB (49367544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fdb20cdfe82256e6da212f948bfc0b6204d8de0f449e216c6b9afc65cdfa11`  
		Last Modified: Wed, 11 Dec 2024 20:31:54 GMT  
		Size: 1.2 MB (1221678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8edf925ff8cff435a926ee74aeb9053ceb1005b17220224e192fd48aa34b8d`  
		Last Modified: Wed, 11 Dec 2024 20:32:55 GMT  
		Size: 150.2 MB (150230607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:66a8ad0443624d2f28a380089001c09579106128d7b1338564ad458ab8c07de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a26665b8684b2c9af56906e7c5646e2582d44726ef343bafb8e4360282ce106`

```dockerfile
```

-	Layers:
	-	`sha256:73ca1098fde4ca6b5cd9a735f77a0aeff5c6966d555450e54329692bc42047f3`  
		Last Modified: Wed, 11 Dec 2024 20:32:48 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f92323307d136fb897c38a14981d2507d11d44b4cc0df6dd01e71ca0805e144b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300891299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1428f2a674ec67789edcafc2534a444a21feebf62427ad9073b72695e3a1ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6757867feefaec653e8deda69d53e16020a2424f9ee2f8815f1031a19dddb3c5`  
		Last Modified: Wed, 11 Dec 2024 20:36:36 GMT  
		Size: 54.5 MB (54478832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f787b3f2c091d822f543fd3294bf3ca088e2876dcea384d170870bef119f6`  
		Last Modified: Wed, 11 Dec 2024 20:36:34 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7162579a043fe7c05532fec8d722108b57e9ceaaeb439818c5e098ceeaa677`  
		Last Modified: Wed, 11 Dec 2024 20:37:30 GMT  
		Size: 216.9 MB (216865596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c2233f8529b1c2577af9165d99da0eeec282c6db13c62cf57cfef7f3a34959c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18d9648f5909cecd8aaeb7087dbeff8e01c325803f9be97c44cce340fcb6425`

```dockerfile
```

-	Layers:
	-	`sha256:923564f8f57ebc6559a3f01ada4d54463906c0076fdfa059450e25a3db526395`  
		Last Modified: Wed, 11 Dec 2024 20:37:25 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:b677df29e01bca3a2d5bdaffe204498834d56a4ed38ff56c0ac6a42d6541b58e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:89d0c76830a904c54ee083cc3fc309b74d2a093cf1c19094efa39175aa47ccba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311926703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ab72e835098264eaccaf9d36af3f73a3be5f1eaa229064f889f2c59502fc3f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe1c9dc9a62b9b03e26e5f698337db83977923b95cad319712946aeb76dc94c`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 54.7 MB (54711978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af5745f3bebd959ed457c5f7f49c51f08a7bbca8de37cfd105cf2aafcc49bb1`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 1.8 MB (1796915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307d269833d4eb7a10befbc2936a876730b0755a0ab928e7f793ef8b3350db76`  
		Last Modified: Wed, 11 Dec 2024 20:29:34 GMT  
		Size: 227.2 MB (227186198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:1731fb9dbe2205720526f7ec0c456aef42300fd95e467030f58672329f71c8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00936e8602fa8edea3058113a9dfd2bdf31200b47b9e3632718775af423b793`

```dockerfile
```

-	Layers:
	-	`sha256:09193c3748b9697ba9e39e24377e2364e45ef2894dae11b7222f3f68941d4c9b`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:608724c5a50ccafe28198eb03e81b90ace815ba07b9755785fa8e37c2d46a844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210219892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419ec34076f0acf55292fc5bda714f829c3d82da6abe215251af0fccbdcde7dd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec725be604fe98fdc7830e882774c71ae85e4282ccd0eb5f45ad4d90484691e`  
		Last Modified: Wed, 11 Dec 2024 20:31:55 GMT  
		Size: 49.4 MB (49367544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fdb20cdfe82256e6da212f948bfc0b6204d8de0f449e216c6b9afc65cdfa11`  
		Last Modified: Wed, 11 Dec 2024 20:31:54 GMT  
		Size: 1.2 MB (1221678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc76c0501b81aa5a269d87798b170cc8c6411f69f6bfd881f4f3fd7785127c41`  
		Last Modified: Wed, 11 Dec 2024 20:31:58 GMT  
		Size: 135.7 MB (135697050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:660145c166a99a62c92b8d96289353e919693b629bcfd5f78bff30081ab9ddff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8683c04579605303c83c75269e209c639702ea12234ac3d306b85646b077d0`

```dockerfile
```

-	Layers:
	-	`sha256:46a735ef5118294321debc658c3abc00c1984632db49a3a2d95d926ca4df717c`  
		Last Modified: Wed, 11 Dec 2024 20:31:54 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:1d8863b5fa6081006bb5d26b9b29a33c6dbcae0ebf6095011ab229c68c35c35c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310386961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fe4e73074f5d44da2ab84d4e50a3d0d7f9e83d1df6c12c958caf55c1057178`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6757867feefaec653e8deda69d53e16020a2424f9ee2f8815f1031a19dddb3c5`  
		Last Modified: Wed, 11 Dec 2024 20:36:36 GMT  
		Size: 54.5 MB (54478832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f787b3f2c091d822f543fd3294bf3ca088e2876dcea384d170870bef119f6`  
		Last Modified: Wed, 11 Dec 2024 20:36:34 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d77bd7a2ae9ad4ce0e7bfa0635a31081b689507123394d8b35d6b205aa7843`  
		Last Modified: Wed, 11 Dec 2024 20:36:39 GMT  
		Size: 226.4 MB (226361258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:36927f0f0b22c05258d7d4750af7cd02e396a9f22685581174fdd9bbe73c8536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75ff5867af0a09bde531ecc8ffcc18cbe93ef71a4ed4a826b0334b54fb49e1a`

```dockerfile
```

-	Layers:
	-	`sha256:f2d85f90c43e75387b0cbfdcb0959831e067adbd9bf0833eed609e02bcf190ce`  
		Last Modified: Wed, 11 Dec 2024 20:36:34 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:b677df29e01bca3a2d5bdaffe204498834d56a4ed38ff56c0ac6a42d6541b58e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:89d0c76830a904c54ee083cc3fc309b74d2a093cf1c19094efa39175aa47ccba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311926703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ab72e835098264eaccaf9d36af3f73a3be5f1eaa229064f889f2c59502fc3f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe1c9dc9a62b9b03e26e5f698337db83977923b95cad319712946aeb76dc94c`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 54.7 MB (54711978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af5745f3bebd959ed457c5f7f49c51f08a7bbca8de37cfd105cf2aafcc49bb1`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 1.8 MB (1796915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307d269833d4eb7a10befbc2936a876730b0755a0ab928e7f793ef8b3350db76`  
		Last Modified: Wed, 11 Dec 2024 20:29:34 GMT  
		Size: 227.2 MB (227186198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1731fb9dbe2205720526f7ec0c456aef42300fd95e467030f58672329f71c8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00936e8602fa8edea3058113a9dfd2bdf31200b47b9e3632718775af423b793`

```dockerfile
```

-	Layers:
	-	`sha256:09193c3748b9697ba9e39e24377e2364e45ef2894dae11b7222f3f68941d4c9b`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:608724c5a50ccafe28198eb03e81b90ace815ba07b9755785fa8e37c2d46a844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210219892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419ec34076f0acf55292fc5bda714f829c3d82da6abe215251af0fccbdcde7dd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec725be604fe98fdc7830e882774c71ae85e4282ccd0eb5f45ad4d90484691e`  
		Last Modified: Wed, 11 Dec 2024 20:31:55 GMT  
		Size: 49.4 MB (49367544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fdb20cdfe82256e6da212f948bfc0b6204d8de0f449e216c6b9afc65cdfa11`  
		Last Modified: Wed, 11 Dec 2024 20:31:54 GMT  
		Size: 1.2 MB (1221678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc76c0501b81aa5a269d87798b170cc8c6411f69f6bfd881f4f3fd7785127c41`  
		Last Modified: Wed, 11 Dec 2024 20:31:58 GMT  
		Size: 135.7 MB (135697050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:660145c166a99a62c92b8d96289353e919693b629bcfd5f78bff30081ab9ddff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8683c04579605303c83c75269e209c639702ea12234ac3d306b85646b077d0`

```dockerfile
```

-	Layers:
	-	`sha256:46a735ef5118294321debc658c3abc00c1984632db49a3a2d95d926ca4df717c`  
		Last Modified: Wed, 11 Dec 2024 20:31:54 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:1d8863b5fa6081006bb5d26b9b29a33c6dbcae0ebf6095011ab229c68c35c35c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310386961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fe4e73074f5d44da2ab84d4e50a3d0d7f9e83d1df6c12c958caf55c1057178`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6757867feefaec653e8deda69d53e16020a2424f9ee2f8815f1031a19dddb3c5`  
		Last Modified: Wed, 11 Dec 2024 20:36:36 GMT  
		Size: 54.5 MB (54478832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f787b3f2c091d822f543fd3294bf3ca088e2876dcea384d170870bef119f6`  
		Last Modified: Wed, 11 Dec 2024 20:36:34 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d77bd7a2ae9ad4ce0e7bfa0635a31081b689507123394d8b35d6b205aa7843`  
		Last Modified: Wed, 11 Dec 2024 20:36:39 GMT  
		Size: 226.4 MB (226361258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:36927f0f0b22c05258d7d4750af7cd02e396a9f22685581174fdd9bbe73c8536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75ff5867af0a09bde531ecc8ffcc18cbe93ef71a4ed4a826b0334b54fb49e1a`

```dockerfile
```

-	Layers:
	-	`sha256:f2d85f90c43e75387b0cbfdcb0959831e067adbd9bf0833eed609e02bcf190ce`  
		Last Modified: Wed, 11 Dec 2024 20:36:34 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:b677df29e01bca3a2d5bdaffe204498834d56a4ed38ff56c0ac6a42d6541b58e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:89d0c76830a904c54ee083cc3fc309b74d2a093cf1c19094efa39175aa47ccba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311926703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ab72e835098264eaccaf9d36af3f73a3be5f1eaa229064f889f2c59502fc3f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe1c9dc9a62b9b03e26e5f698337db83977923b95cad319712946aeb76dc94c`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 54.7 MB (54711978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af5745f3bebd959ed457c5f7f49c51f08a7bbca8de37cfd105cf2aafcc49bb1`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 1.8 MB (1796915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307d269833d4eb7a10befbc2936a876730b0755a0ab928e7f793ef8b3350db76`  
		Last Modified: Wed, 11 Dec 2024 20:29:34 GMT  
		Size: 227.2 MB (227186198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:1731fb9dbe2205720526f7ec0c456aef42300fd95e467030f58672329f71c8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00936e8602fa8edea3058113a9dfd2bdf31200b47b9e3632718775af423b793`

```dockerfile
```

-	Layers:
	-	`sha256:09193c3748b9697ba9e39e24377e2364e45ef2894dae11b7222f3f68941d4c9b`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:608724c5a50ccafe28198eb03e81b90ace815ba07b9755785fa8e37c2d46a844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210219892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419ec34076f0acf55292fc5bda714f829c3d82da6abe215251af0fccbdcde7dd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec725be604fe98fdc7830e882774c71ae85e4282ccd0eb5f45ad4d90484691e`  
		Last Modified: Wed, 11 Dec 2024 20:31:55 GMT  
		Size: 49.4 MB (49367544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fdb20cdfe82256e6da212f948bfc0b6204d8de0f449e216c6b9afc65cdfa11`  
		Last Modified: Wed, 11 Dec 2024 20:31:54 GMT  
		Size: 1.2 MB (1221678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc76c0501b81aa5a269d87798b170cc8c6411f69f6bfd881f4f3fd7785127c41`  
		Last Modified: Wed, 11 Dec 2024 20:31:58 GMT  
		Size: 135.7 MB (135697050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:660145c166a99a62c92b8d96289353e919693b629bcfd5f78bff30081ab9ddff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8683c04579605303c83c75269e209c639702ea12234ac3d306b85646b077d0`

```dockerfile
```

-	Layers:
	-	`sha256:46a735ef5118294321debc658c3abc00c1984632db49a3a2d95d926ca4df717c`  
		Last Modified: Wed, 11 Dec 2024 20:31:54 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:1d8863b5fa6081006bb5d26b9b29a33c6dbcae0ebf6095011ab229c68c35c35c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310386961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fe4e73074f5d44da2ab84d4e50a3d0d7f9e83d1df6c12c958caf55c1057178`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6757867feefaec653e8deda69d53e16020a2424f9ee2f8815f1031a19dddb3c5`  
		Last Modified: Wed, 11 Dec 2024 20:36:36 GMT  
		Size: 54.5 MB (54478832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f787b3f2c091d822f543fd3294bf3ca088e2876dcea384d170870bef119f6`  
		Last Modified: Wed, 11 Dec 2024 20:36:34 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d77bd7a2ae9ad4ce0e7bfa0635a31081b689507123394d8b35d6b205aa7843`  
		Last Modified: Wed, 11 Dec 2024 20:36:39 GMT  
		Size: 226.4 MB (226361258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:36927f0f0b22c05258d7d4750af7cd02e396a9f22685581174fdd9bbe73c8536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75ff5867af0a09bde531ecc8ffcc18cbe93ef71a4ed4a826b0334b54fb49e1a`

```dockerfile
```

-	Layers:
	-	`sha256:f2d85f90c43e75387b0cbfdcb0959831e067adbd9bf0833eed609e02bcf190ce`  
		Last Modified: Wed, 11 Dec 2024 20:36:34 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:b677df29e01bca3a2d5bdaffe204498834d56a4ed38ff56c0ac6a42d6541b58e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:89d0c76830a904c54ee083cc3fc309b74d2a093cf1c19094efa39175aa47ccba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311926703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ab72e835098264eaccaf9d36af3f73a3be5f1eaa229064f889f2c59502fc3f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe1c9dc9a62b9b03e26e5f698337db83977923b95cad319712946aeb76dc94c`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 54.7 MB (54711978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af5745f3bebd959ed457c5f7f49c51f08a7bbca8de37cfd105cf2aafcc49bb1`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 1.8 MB (1796915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307d269833d4eb7a10befbc2936a876730b0755a0ab928e7f793ef8b3350db76`  
		Last Modified: Wed, 11 Dec 2024 20:29:34 GMT  
		Size: 227.2 MB (227186198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1731fb9dbe2205720526f7ec0c456aef42300fd95e467030f58672329f71c8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00936e8602fa8edea3058113a9dfd2bdf31200b47b9e3632718775af423b793`

```dockerfile
```

-	Layers:
	-	`sha256:09193c3748b9697ba9e39e24377e2364e45ef2894dae11b7222f3f68941d4c9b`  
		Last Modified: Wed, 11 Dec 2024 20:29:31 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:608724c5a50ccafe28198eb03e81b90ace815ba07b9755785fa8e37c2d46a844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210219892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419ec34076f0acf55292fc5bda714f829c3d82da6abe215251af0fccbdcde7dd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec725be604fe98fdc7830e882774c71ae85e4282ccd0eb5f45ad4d90484691e`  
		Last Modified: Wed, 11 Dec 2024 20:31:55 GMT  
		Size: 49.4 MB (49367544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fdb20cdfe82256e6da212f948bfc0b6204d8de0f449e216c6b9afc65cdfa11`  
		Last Modified: Wed, 11 Dec 2024 20:31:54 GMT  
		Size: 1.2 MB (1221678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc76c0501b81aa5a269d87798b170cc8c6411f69f6bfd881f4f3fd7785127c41`  
		Last Modified: Wed, 11 Dec 2024 20:31:58 GMT  
		Size: 135.7 MB (135697050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:660145c166a99a62c92b8d96289353e919693b629bcfd5f78bff30081ab9ddff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8683c04579605303c83c75269e209c639702ea12234ac3d306b85646b077d0`

```dockerfile
```

-	Layers:
	-	`sha256:46a735ef5118294321debc658c3abc00c1984632db49a3a2d95d926ca4df717c`  
		Last Modified: Wed, 11 Dec 2024 20:31:54 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:1d8863b5fa6081006bb5d26b9b29a33c6dbcae0ebf6095011ab229c68c35c35c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310386961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fe4e73074f5d44da2ab84d4e50a3d0d7f9e83d1df6c12c958caf55c1057178`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6757867feefaec653e8deda69d53e16020a2424f9ee2f8815f1031a19dddb3c5`  
		Last Modified: Wed, 11 Dec 2024 20:36:36 GMT  
		Size: 54.5 MB (54478832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f787b3f2c091d822f543fd3294bf3ca088e2876dcea384d170870bef119f6`  
		Last Modified: Wed, 11 Dec 2024 20:36:34 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d77bd7a2ae9ad4ce0e7bfa0635a31081b689507123394d8b35d6b205aa7843`  
		Last Modified: Wed, 11 Dec 2024 20:36:39 GMT  
		Size: 226.4 MB (226361258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:36927f0f0b22c05258d7d4750af7cd02e396a9f22685581174fdd9bbe73c8536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75ff5867af0a09bde531ecc8ffcc18cbe93ef71a4ed4a826b0334b54fb49e1a`

```dockerfile
```

-	Layers:
	-	`sha256:f2d85f90c43e75387b0cbfdcb0959831e067adbd9bf0833eed609e02bcf190ce`  
		Last Modified: Wed, 11 Dec 2024 20:36:34 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json
