## `dart:beta-sdk`

```console
$ docker pull dart@sha256:32c1007130490cf1e1bcbf46b3b5150667771abf4ac0dd6cf2cd47acff2851d4
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
$ docker pull dart@sha256:d21296a3f5efa4767ea6a1cc2030a1f6f357201e32fb9bc836e8947b553e419f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285788080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7503e956699a9ae2534340be153107fdf9fac8f9e59733892272e09a658dd11e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Apr 2025 07:27:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6f53574f123efcf43659030f18038f460fa976ed1b12e66bffa991f7d5ad87c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6456bfdd97f3c0ea76890aa0847fb1ea90c5a95551481db7f1bc98fcefde9368;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9576dcf1595514b434b65620d7dae86df1813e2be084c176233031e0848cdc69;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-278.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f8d425d2158f7080012be3f01d16c145749ffd5ffc0d4af3ab397369d693d1`  
		Last Modified: Mon, 28 Apr 2025 21:56:07 GMT  
		Size: 54.9 MB (54906126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957c64a25be43b7422c3ee83430b8f292618afe9786aea0819726052137d35eb`  
		Last Modified: Mon, 28 Apr 2025 21:56:06 GMT  
		Size: 1.8 MB (1785447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d903a52d13dd78a6b7e67c821228a7b54e7ce3e04a0680ee808262c5e1bb4ed`  
		Last Modified: Mon, 28 Apr 2025 21:56:09 GMT  
		Size: 200.9 MB (200868833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:66f17b37124726266a0144f7672b4b2a297a68f9bfd7e7241a4fe0b00479703c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79506e1935de096e08f9edfbf021b877c3747fe2f4705f0725ccc36d11542665`

```dockerfile
```

-	Layers:
	-	`sha256:7e2f449adf87d7b9ab6b13a6ae8d21455a9ca7f45deba0610f48837d70bfeb57`  
		Last Modified: Mon, 28 Apr 2025 21:56:06 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:fcb47073dc94621c6ee4d513866089c33fd9893d25126149f2c1e70da55b3373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 MB (216564329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f8af776f699b9124d934d1173111f12cf206f113e253191f482cb27930f8ff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6f53574f123efcf43659030f18038f460fa976ed1b12e66bffa991f7d5ad87c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6456bfdd97f3c0ea76890aa0847fb1ea90c5a95551481db7f1bc98fcefde9368;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9576dcf1595514b434b65620d7dae86df1813e2be084c176233031e0848cdc69;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-278.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1330b2381da106ae28676390c114d27603e3d27780aa9cf44a256c87c17d3f73`  
		Last Modified: Thu, 17 Apr 2025 18:50:34 GMT  
		Size: 51.7 MB (51680929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa2189d0ec2c0aa10e7cd73369cd1a292f801f44dae53b2dca0bfc1de42f32b`  
		Last Modified: Thu, 17 Apr 2025 18:50:33 GMT  
		Size: 1.2 MB (1221946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152c9675305586ea17ae1bd95e07c9e788b32963793efccdf9ab297de4f1d357`  
		Last Modified: Thu, 17 Apr 2025 18:51:27 GMT  
		Size: 139.7 MB (139723555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:be4678b09c641f67f4b19cd85aad2b186c33406b672afae4bdf7da3e224c687a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47386101b1d0dffefb59ddd5a9a1d9591b880c9dba256c4a7d74d23c2c1c4a21`

```dockerfile
```

-	Layers:
	-	`sha256:54fc3aece1519b5e1abdae77d66a61e8447fd4c981d48dc5aaef1d86811bd383`  
		Last Modified: Thu, 17 Apr 2025 18:51:23 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f9621984605a97e45161dce06d8ede6a6f8564baf5c6d9c2a62bf9e37d2b5a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286624838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4730ca61f6c14f7dc16632ba527dbb68c06f40bf5405e009546b3982ef83e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6f53574f123efcf43659030f18038f460fa976ed1b12e66bffa991f7d5ad87c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6456bfdd97f3c0ea76890aa0847fb1ea90c5a95551481db7f1bc98fcefde9368;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9576dcf1595514b434b65620d7dae86df1813e2be084c176233031e0848cdc69;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-278.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121cece50d49eba8634dea84f9d28d9736feef46609fad36256ab2fc13bda939`  
		Last Modified: Thu, 17 Apr 2025 18:53:22 GMT  
		Size: 56.9 MB (56943757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d5a6d2921a02dc94eeacce2d2369f9b7aec957f761943a2539a79879077d8c`  
		Last Modified: Thu, 17 Apr 2025 18:53:21 GMT  
		Size: 1.5 MB (1488213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e41e5b9170f5ef4469004795bdb5d6c8daf9ce7caec4c0440fa2f8b8a8cf8`  
		Last Modified: Thu, 17 Apr 2025 18:54:16 GMT  
		Size: 200.1 MB (200126516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:357ebbe44ef68afe36703bef276ae735361ec0f4f6dc95b64fe6016ddbb07534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7f6ec38a3630af168ebe1066bf0afe2303fd4b91a5188282f7b613d5a084bc`

```dockerfile
```

-	Layers:
	-	`sha256:0a820c2eb9f30b9693d721b611121f5e4440f0de136ee144e9010d4e6810fb75`  
		Last Modified: Thu, 17 Apr 2025 18:54:09 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json
