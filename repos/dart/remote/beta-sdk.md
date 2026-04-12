## `dart:beta-sdk`

```console
$ docker pull dart@sha256:f8e8192a6bc455df9a5ad5a683c14511252ca1941998cfabd14df5550f5e6997
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:c868a606de90ebbb2d7c9169604e95b26d9e31faa0b9628169a4e97c31207264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.9 MB (313898836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc4f3a45f8ca1e988d345af9e942d7687e8e2e52c60567016e390e43fc8c2c8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 17:48:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Apr 2026 17:48:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 10 Apr 2026 17:48:07 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 10 Apr 2026 17:48:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Apr 2026 17:48:07 GMT
WORKDIR /root
# Fri, 10 Apr 2026 17:48:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8ca58464d189e83f050b08315355c198cf593843c971c17600e2b2ee11d6984c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ef718700ec8dc7d361655b3bda9b943a815dc5069ffef2f8e57050251c8ed4be;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ce436dd4aefff9ffc777c1d566f97272bda3d08544457ca8f0ec69fc8e19ad;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9c3aa74219443e88c37a362d9615a3d235525f35f3439efdc0e6555f7ecb9827;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd6c9f3eb01852c6478ef4cd50b57ad35670913fcf4c257b2dcd9637a921833`  
		Last Modified: Fri, 10 Apr 2026 17:48:46 GMT  
		Size: 45.5 MB (45465995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7287f7d8b709322723138c7b7a5ecf4b843f490432c5dbe24ffdef2a1540fecf`  
		Last Modified: Fri, 10 Apr 2026 17:48:44 GMT  
		Size: 1.9 MB (1869568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc28339dcc17b292f7a6d597e83589b66524c1cad8e7b99b55ac70a9093c58c`  
		Last Modified: Fri, 10 Apr 2026 17:48:50 GMT  
		Size: 236.8 MB (236787601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b6a79b61cd955e2a68f10018b7507e6223a80eff7f13be339383138df3f5ba19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780e48a7cb1835ebc8bdf8e0330a58e4cb639d719d83aefbcdebff856c41d4d2`

```dockerfile
```

-	Layers:
	-	`sha256:00c01ad7a565f9e20014dbd71534de871dee0493fdb8d5fbe177dbe66d81a1f8`  
		Last Modified: Fri, 10 Apr 2026 17:48:44 GMT  
		Size: 18.9 KB (18922 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:4251b09021e826e1fb17f1e3bee4d145daa252daff6ba41c30d48853264b3e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228285459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6dca11b037e4ebbd4a7cd5de38f381c4d46c7a5e98d93dc73a9fd45364c5847`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 17:11:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Apr 2026 17:11:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 10 Apr 2026 17:11:32 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 10 Apr 2026 17:11:32 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Apr 2026 17:11:32 GMT
WORKDIR /root
# Fri, 10 Apr 2026 17:12:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8ca58464d189e83f050b08315355c198cf593843c971c17600e2b2ee11d6984c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ef718700ec8dc7d361655b3bda9b943a815dc5069ffef2f8e57050251c8ed4be;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ce436dd4aefff9ffc777c1d566f97272bda3d08544457ca8f0ec69fc8e19ad;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9c3aa74219443e88c37a362d9615a3d235525f35f3439efdc0e6555f7ecb9827;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e5bacabb360e6b22df30d9b98f96c7189a2f541937f89e115c874666372170`  
		Last Modified: Fri, 10 Apr 2026 17:12:01 GMT  
		Size: 39.7 MB (39713299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263bffd7ebff414a443520e64e05b25a58d7abd02c25cfd9337b2e4362a46d04`  
		Last Modified: Fri, 10 Apr 2026 17:12:00 GMT  
		Size: 1.3 MB (1273158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee82d451abd3a5f696b3f35950d3387d274b6337b3d83c0fea6408b33dd2773`  
		Last Modified: Fri, 10 Apr 2026 17:12:43 GMT  
		Size: 161.1 MB (161089317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ccc008f5a00eda8405fa39f9a0ee8eeff37fe319d1eb572e7fea130d05fbd7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6fa857cdfe230a4d76efdca2ff08200a01405990e48d29b2833aeddc4ffbac`

```dockerfile
```

-	Layers:
	-	`sha256:9ef800589278591cab9c9532dab8db12de6a27203140f46ef4b20c0b5e24561c`  
		Last Modified: Fri, 10 Apr 2026 17:12:40 GMT  
		Size: 19.0 KB (19028 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:5e2fcb3c131d8cbcb66a3caf0fe9444edea2affd5776cb755786663d3116314e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312702136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7daec8f294fe55d7865514f6d4ef3953ef3f6f1082122a2484a1890932800f0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 17:12:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Apr 2026 17:12:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 10 Apr 2026 17:12:44 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 10 Apr 2026 17:12:44 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Apr 2026 17:12:44 GMT
WORKDIR /root
# Fri, 10 Apr 2026 17:12:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8ca58464d189e83f050b08315355c198cf593843c971c17600e2b2ee11d6984c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ef718700ec8dc7d361655b3bda9b943a815dc5069ffef2f8e57050251c8ed4be;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ce436dd4aefff9ffc777c1d566f97272bda3d08544457ca8f0ec69fc8e19ad;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9c3aa74219443e88c37a362d9615a3d235525f35f3439efdc0e6555f7ecb9827;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1695e8dac7d08cf7c0282fa76c270064d1fd80f966a8e51e5a36139973e599b1`  
		Last Modified: Fri, 10 Apr 2026 17:13:28 GMT  
		Size: 45.6 MB (45617172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121a8696dbc2b5c0a5706cf6a7d51c1f86862878435c0b5985ad1daf581be87b`  
		Last Modified: Fri, 10 Apr 2026 17:13:27 GMT  
		Size: 1.6 MB (1564360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54316ca21e446ac74ade6e7bfd1c513337fcd422a061194c35fe744fc613de2`  
		Last Modified: Fri, 10 Apr 2026 17:13:32 GMT  
		Size: 235.4 MB (235382021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:83862796a33d7f0a0dcf38f0efc6a722e9e82f60419b50427efa212c9bb81c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb49c7fcb2e3c78a1bcbd0d920e33455e04945828bb13fc3f53205cec8429280`

```dockerfile
```

-	Layers:
	-	`sha256:27fd078413c2e443672f2a31ec50e74154321edf5b4cc77b4e96b3e11ba0fa8e`  
		Last Modified: Fri, 10 Apr 2026 17:13:27 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:eb5824614a555b5efec636564f757db5f2db21695754a84a83783759f8b5b351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250927949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10354152681ed59e19b06735869aa419e39ff1cf748822f6f833a1050e140487`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sun, 12 Apr 2026 09:45:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 12 Apr 2026 09:46:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Sun, 12 Apr 2026 09:46:00 GMT
ENV DART_SDK=/usr/lib/dart
# Sun, 12 Apr 2026 09:46:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 12 Apr 2026 09:46:00 GMT
WORKDIR /root
# Sun, 12 Apr 2026 09:52:41 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8ca58464d189e83f050b08315355c198cf593843c971c17600e2b2ee11d6984c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ef718700ec8dc7d361655b3bda9b943a815dc5069ffef2f8e57050251c8ed4be;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ce436dd4aefff9ffc777c1d566f97272bda3d08544457ca8f0ec69fc8e19ad;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9c3aa74219443e88c37a362d9615a3d235525f35f3439efdc0e6555f7ecb9827;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0dfbd6705fae98ed0e247af95b61f3560a865a45bae2055794e77062136d997`  
		Last Modified: Sun, 12 Apr 2026 09:51:07 GMT  
		Size: 44.2 MB (44183529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c9cf140c22c9e3b48a0177b4c2319226ac6b55b287c20dda6297a3de832d65`  
		Last Modified: Sun, 12 Apr 2026 09:50:55 GMT  
		Size: 1.6 MB (1564390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fd1fcd7f6e9b9817b7a3b4f1bd857c8b37a47faf03be9e2ed2e29387408ac4`  
		Last Modified: Sun, 12 Apr 2026 09:57:05 GMT  
		Size: 176.9 MB (176904220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:3f74a7371df2ad2e01a00759d4f8ead6a2affae44470c41286e0ea7b3ccaaf51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc4715a9c0c916242a823a2c430c86829182c0749aa4913a5ced7214910d7f3`

```dockerfile
```

-	Layers:
	-	`sha256:2fe7ba05f04f181d7db9284e16823c62a2d325b818c8a588a44e01718151cf8c`  
		Last Modified: Sun, 12 Apr 2026 09:56:39 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json
