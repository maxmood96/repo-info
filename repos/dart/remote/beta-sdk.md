## `dart:beta-sdk`

```console
$ docker pull dart@sha256:2b24bf41ef25ed490d81eb6e9cc85667c5214896b87bededcbeaf2a0eb11c479
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
$ docker pull dart@sha256:71b375f5e6c13ba5bf8dd6195769369f8be2e562762e4707a59dee3222d4946a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288384242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6e6f4403957060e2890e91f26a3cb6279dbdd7576b5112b807d374f11c4d5d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Wed, 05 Nov 2025 19:25:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 19:25:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 05 Nov 2025 19:25:07 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 05 Nov 2025 19:25:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 19:25:07 GMT
WORKDIR /root
# Wed, 05 Nov 2025 19:25:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4becf5c692812de85faae19461d64078094491b34e58d9d5f36bd0f8fc989866;             SDK_ARCH="x64";;         armhf)             DART_SHA256=378e6683e3b70289193fb17052630ce0439fb3b5937c52aeba7718c371c04c8b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=24dc3ac9faf1baa673a106586dfd2682739ae060405fa3f1cbc991b4c698904e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3f0c1e38978020aca98275cc5785b6766b76b376469c563901d2555046731f04;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4042dd0303666dacecb7f6ca85663367bef494b45f8e60bf8725119f2f0344ef`  
		Last Modified: Wed, 05 Nov 2025 19:26:02 GMT  
		Size: 42.5 MB (42493410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16025c2e75678acccfcfc398d6f8bbd0fb49558ef221423d96d96d6083889bc4`  
		Last Modified: Wed, 05 Nov 2025 19:25:55 GMT  
		Size: 1.9 MB (1873623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e640fe4d1143ee8a64d9b0f6534932c8073fc418d9c418aa12078842ff2378e`  
		Last Modified: Wed, 05 Nov 2025 21:53:52 GMT  
		Size: 214.2 MB (214239073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ee0a6253592a88a6224f07ab6b93cd85d479c9b53264b5aa75b4843c95b6d8aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdd828d065af5b117651e39876902901fd06874268023d49944b7ab3e2bd932`

```dockerfile
```

-	Layers:
	-	`sha256:683f78dbf7affe7da0806fe1402dc72ef1f1ac31c5abdb64cfc694afc8f94c49`  
		Last Modified: Wed, 05 Nov 2025 21:53:23 GMT  
		Size: 18.9 KB (18918 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:f4164b3d8af46f8847a3f6811a3e3814b1a28a00af21060786de5e98d39a7952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220617190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a80d1cac11117c49585971491fa7a28c8e7db95b9e41ba4b2497d9e78df6aa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Wed, 05 Nov 2025 18:53:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 18:53:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 05 Nov 2025 18:53:25 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 05 Nov 2025 18:53:25 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 18:53:25 GMT
WORKDIR /root
# Wed, 05 Nov 2025 18:53:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4becf5c692812de85faae19461d64078094491b34e58d9d5f36bd0f8fc989866;             SDK_ARCH="x64";;         armhf)             DART_SHA256=378e6683e3b70289193fb17052630ce0439fb3b5937c52aeba7718c371c04c8b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=24dc3ac9faf1baa673a106586dfd2682739ae060405fa3f1cbc991b4c698904e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3f0c1e38978020aca98275cc5785b6766b76b376469c563901d2555046731f04;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7104bc72ee8087378d2d22b93b7f9c61969f5f41e32321070d4969f33391d9f`  
		Last Modified: Wed, 05 Nov 2025 18:54:07 GMT  
		Size: 37.5 MB (37498698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6edaf786ddf0d7f213c2a02f8d0d0b1b1813900ad8a45baf32a79ef532a300`  
		Last Modified: Wed, 05 Nov 2025 18:54:04 GMT  
		Size: 1.3 MB (1275119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d44030c6c8bf3fe9113d384b6fc11b3b8348c509c5339e1816e5f50eb644f58`  
		Last Modified: Wed, 05 Nov 2025 21:53:58 GMT  
		Size: 155.6 MB (155630302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c655e7eb57450283a8f81961573d507d2778dff1edf2cb376c63b323f7e85a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2a4773d3a6b1df18d48bf0f844caebf4feece98c96ef3e2b447bccc941d25b`

```dockerfile
```

-	Layers:
	-	`sha256:7eaca80efe181dae93c4cb46791aca6dc48c59be433574e3da6536bde6a13dba`  
		Last Modified: Wed, 05 Nov 2025 21:53:26 GMT  
		Size: 19.0 KB (19022 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:407e485f6295107702549e213fa574f8bc334d6a1ef5ae9ed9c470dbac1a0d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287469107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7b9da27b2373009e96c19edfc0b42cdb463b11251a80db40237b39daf4edad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Wed, 05 Nov 2025 18:53:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 18:53:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 05 Nov 2025 18:53:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 05 Nov 2025 18:53:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 18:53:18 GMT
WORKDIR /root
# Wed, 05 Nov 2025 18:53:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4becf5c692812de85faae19461d64078094491b34e58d9d5f36bd0f8fc989866;             SDK_ARCH="x64";;         armhf)             DART_SHA256=378e6683e3b70289193fb17052630ce0439fb3b5937c52aeba7718c371c04c8b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=24dc3ac9faf1baa673a106586dfd2682739ae060405fa3f1cbc991b4c698904e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3f0c1e38978020aca98275cc5785b6766b76b376469c563901d2555046731f04;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0909e2dfa0aaaa4e7f55da92ee4e171b20e668488bb69b219e5a5fd865b81af6`  
		Last Modified: Wed, 05 Nov 2025 18:54:11 GMT  
		Size: 42.3 MB (42292977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2df8c8b2765e33e0fca2c5a8d4189cb5d84845845cf37bde7bfd9d9ac3ad843`  
		Last Modified: Wed, 05 Nov 2025 18:54:07 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63eb89542070eab251f10f1cdf20603b1e244835bc11b0db1fe0055245c469b1`  
		Last Modified: Wed, 05 Nov 2025 21:54:02 GMT  
		Size: 213.5 MB (213467155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:f218058ea7c77c3b398be7cd1417e35fdbfe8c3dde442bced0b596f6a1814c55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ec416bab542f52cc22459b946d4551ceb5251abe55819e92f267d814efc2bb`

```dockerfile
```

-	Layers:
	-	`sha256:44bf119163ba9fd3ce0690154837165fa968bff7285972eba2f7efe75dfaeaf0`  
		Last Modified: Wed, 05 Nov 2025 21:53:30 GMT  
		Size: 19.1 KB (19052 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:64b91a06e3f56dacf2e10ddfc61aee95349733792ec7d328d58270d6cb09e5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232961869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796275d6d7561a9cc86083ad8bd9f5be2491cd3a2921064e6ec2308985ad0976`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Wed, 05 Nov 2025 12:06:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 12:06:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 05 Nov 2025 12:06:29 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 05 Nov 2025 12:06:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 12:06:29 GMT
WORKDIR /root
# Wed, 05 Nov 2025 12:10:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=40132ac8b651895e76011d54d5703cc5a2e126cd396f75a0d9f24729b4f9c79d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bbc36ed5076a95609cccbc6f76f7b077f998acdd4b7f6a22ff66e32412fd5dcf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b440bb5f329c07161ab0396bbc8f739d9c547067cb98b9882932a048bebff62c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=bdc460714c5cefc2984fd0f8fe2c83a907cd15c44d35f43ba8dff3e40a7eb60c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec87d9e6fe2a6c3d564b97ec749845500d1eb36d011fa27e67400daca20cad51`  
		Last Modified: Wed, 05 Nov 2025 12:15:22 GMT  
		Size: 41.6 MB (41560904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12241236d8e9213dd7db34ee23bd2fa4fe14911c837e542a2a0765c13d09ee31`  
		Last Modified: Wed, 05 Nov 2025 12:15:19 GMT  
		Size: 1.6 MB (1567071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15e70182d88b3eba8c914f0befa8131d855ae051a841df10723624ec5908f8d`  
		Last Modified: Wed, 05 Nov 2025 21:54:05 GMT  
		Size: 161.6 MB (161558076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:12c46cb584642a49e5169c6e3fc853712075d24dad2df8dc02ba703caf86ed91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd936ea8cc8b4c240e3a2172e9f3ea99cd998c1dedb38aa3d5a2e0d07a0993c0`

```dockerfile
```

-	Layers:
	-	`sha256:90c2ccd8f3f98c842981f52da07d5376ed5e1db10d0f3eae2f2ec361ebdc20aa`  
		Last Modified: Wed, 05 Nov 2025 21:53:37 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json
