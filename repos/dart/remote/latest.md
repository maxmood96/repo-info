## `dart:latest`

```console
$ docker pull dart@sha256:c39a40fbca1a42073604c8b08b9b5657837e47605961b0931922413e456e3597
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

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:f446306095d784981cc68e751cff0aee10ba5546e1cd28f9701e9257d4ee2fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287265647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a171a651e270572ea570d267296e83a44e685e51ead57a56b58fc9ec2a209c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Tue, 16 Dec 2025 21:38:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Dec 2025 21:38:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 16 Dec 2025 21:38:03 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 16 Dec 2025 21:38:03 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 21:38:03 GMT
WORKDIR /root
# Tue, 16 Dec 2025 21:38:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6c2ec3ec17956bf868255fb30c8f9330dc7615dcbd5df252cc1ceba87aa22735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2bd447cb87dec1584432968b2d1637b466960bd367528287fe907a73854c8c95;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2f4bb013b7efbca6f9178795c2ca4bf1f3d4874abfc18da974566cc2d9a65aec;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=6f9fa3dca28e9b65b76095793054532d346db93ae2ff3a3f5a4211f2cb8d742c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4c5148e5d82dbede36f8de6bfa1b0b2e1ac662b7026ef959651d45b4e31b01`  
		Last Modified: Tue, 16 Dec 2025 21:39:02 GMT  
		Size: 42.5 MB (42494195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9eccf32635aa98b6709c2f9e66629e9b690eab8914736d08c5b3674ee4810a`  
		Last Modified: Tue, 16 Dec 2025 21:38:56 GMT  
		Size: 1.9 MB (1873625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13dcbcc949f6d200c852efbd682a76d0dea2e3c0de0dddac5f40e3bb969c4ac3`  
		Last Modified: Tue, 16 Dec 2025 21:39:25 GMT  
		Size: 213.1 MB (213121299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:8b5e2eaca7dd54cf33bacde7da86046f20240d237beed522fc1afa85c9518568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df371467266a36b71980636326a637f642fa1d865547b62a74da5e6fa05b18e1`

```dockerfile
```

-	Layers:
	-	`sha256:af953167353a38fc4335f27a1e02ddb9d443466ec209b3f3db2fa5e7d942a15e`  
		Last Modified: Tue, 16 Dec 2025 21:53:54 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:a1deb26db4eaff25da86a9783e961cefb886f0882d18467e6bdc2fc5593f96e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219907849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897f67e09d5c4d4b4df9f8ac49dcdf3f03cd441c57ca7b616ab0d9f17105d915`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Tue, 16 Dec 2025 21:38:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Dec 2025 21:38:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 16 Dec 2025 21:38:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 16 Dec 2025 21:38:05 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 21:38:05 GMT
WORKDIR /root
# Tue, 16 Dec 2025 21:38:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6c2ec3ec17956bf868255fb30c8f9330dc7615dcbd5df252cc1ceba87aa22735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2bd447cb87dec1584432968b2d1637b466960bd367528287fe907a73854c8c95;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2f4bb013b7efbca6f9178795c2ca4bf1f3d4874abfc18da974566cc2d9a65aec;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=6f9fa3dca28e9b65b76095793054532d346db93ae2ff3a3f5a4211f2cb8d742c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77a5ecbe829778d081e1255a51742f3ac47546c876317fd7d2756ce9842ce65`  
		Last Modified: Tue, 16 Dec 2025 21:38:51 GMT  
		Size: 37.5 MB (37498376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be3ad922e243e64dd332bbe79a0e9972779ee27288e0afc01e898ef8bbe9b67`  
		Last Modified: Tue, 16 Dec 2025 21:38:49 GMT  
		Size: 1.3 MB (1275121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7ffa003b03c0a4fe6b56a1a5229e52723a91b0f7f789f8eae4046457f8b813`  
		Last Modified: Wed, 17 Dec 2025 02:10:27 GMT  
		Size: 154.9 MB (154924307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:1e63d0b006be96a5fd4753fba4ac99351b95cbafea71731dbd9b580af3e50360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ae188f3213baf2bbcc89bf82255b53217046a378a4da20345c0a0ae65b8e70`

```dockerfile
```

-	Layers:
	-	`sha256:907acf9393367c1126a58e8e6114a611b8eccabb400093a062ca4630110a2f8e`  
		Last Modified: Tue, 16 Dec 2025 21:53:58 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:c6c727e33a4c031de1a3f567334eaa2121e9fe9384652054f9c0e55ab04a2a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286358317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac1dfdea47a0d640489ec7fdc5126339facd663073de2646c74abd52ff72f6d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Tue, 16 Dec 2025 21:37:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Dec 2025 21:37:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 16 Dec 2025 21:37:58 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 16 Dec 2025 21:37:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 21:37:58 GMT
WORKDIR /root
# Tue, 16 Dec 2025 21:38:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6c2ec3ec17956bf868255fb30c8f9330dc7615dcbd5df252cc1ceba87aa22735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2bd447cb87dec1584432968b2d1637b466960bd367528287fe907a73854c8c95;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2f4bb013b7efbca6f9178795c2ca4bf1f3d4874abfc18da974566cc2d9a65aec;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=6f9fa3dca28e9b65b76095793054532d346db93ae2ff3a3f5a4211f2cb8d742c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694db15c500a08dd58a046be768dbe1507bfc58be2b11db29d2da0a71cb0e503`  
		Last Modified: Tue, 16 Dec 2025 21:38:59 GMT  
		Size: 42.3 MB (42293289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe136d9b219df38ad5274cd601f2ff608903fd5847148d84c8b4adfd508d37d`  
		Last Modified: Tue, 16 Dec 2025 21:38:57 GMT  
		Size: 1.6 MB (1566654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc8f3aac845cb0f6965b6b64d72bab6862e0c94cbe7ce4242a890b59f57d305`  
		Last Modified: Tue, 16 Dec 2025 21:39:01 GMT  
		Size: 212.4 MB (212359714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:14601bd80b6cebf63abccff24a099d84e7e285c196659fe5367c84a683c8faee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc274c840317e6ba0b8d05d928710cdff39291722997e68690156f2c425a32a`

```dockerfile
```

-	Layers:
	-	`sha256:f039c2978df4c3b2acbb77e5fcc7bb70c998f1299fe18a00ed7ebb7f8d87996d`  
		Last Modified: Tue, 16 Dec 2025 21:54:01 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; riscv64

```console
$ docker pull dart@sha256:ccfa666b54713a075f6b6458645998cda74c3676926e1e0360dee33387abf7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232963314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5507127a82d6aed808b02bbd40ba2fb8a6a018423bc7af35f12a04b41fc2b1f4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Tue, 16 Dec 2025 21:39:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Dec 2025 21:39:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 16 Dec 2025 21:39:53 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 16 Dec 2025 21:39:53 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 21:39:53 GMT
WORKDIR /root
# Tue, 16 Dec 2025 21:40:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6c2ec3ec17956bf868255fb30c8f9330dc7615dcbd5df252cc1ceba87aa22735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2bd447cb87dec1584432968b2d1637b466960bd367528287fe907a73854c8c95;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2f4bb013b7efbca6f9178795c2ca4bf1f3d4874abfc18da974566cc2d9a65aec;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=6f9fa3dca28e9b65b76095793054532d346db93ae2ff3a3f5a4211f2cb8d742c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81585f83045cc5025da0825baddf7cace696ba02542427e22e87c17a96ea4a32`  
		Last Modified: Tue, 16 Dec 2025 21:45:01 GMT  
		Size: 41.6 MB (41560781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016b0c22ecb0562043eb7b92afb0d0c1d9871687a4afc9b04fd38a9530234772`  
		Last Modified: Tue, 16 Dec 2025 21:44:57 GMT  
		Size: 1.6 MB (1567079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8282540ba9efd9e2070115cc834e1cf08a8f1ea5321aebb1b8c05c6393b498a1`  
		Last Modified: Tue, 16 Dec 2025 21:45:14 GMT  
		Size: 161.6 MB (161562266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:1ea96f807be99d275cdcff73ad8e25cdd74232276776158b94b7fab50d3a1b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10663443cf092c337c0ce8b75797cbbdda8940889ecdc138d72a08bc5d18717c`

```dockerfile
```

-	Layers:
	-	`sha256:2a250d750b9d103537127b659fdb28160ebed97c6931d6f9ee66e682780b6d9d`  
		Last Modified: Tue, 16 Dec 2025 21:54:15 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json
