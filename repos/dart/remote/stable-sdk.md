## `dart:stable-sdk`

```console
$ docker pull dart@sha256:51578795746b2aa2e80019c11895414a35f6be69903ce4485de717dfa1b7ce6b
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

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:0a423a33be776e7632bdd7134f3f8d5aeaa4701ff2256ea7b06a9ff14bf3795b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310946643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b5a1e0d241b7ca503cf8d7120384da7e0f8f6fc3c60522bf76176d8f22389d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 19 May 2026 23:23:52 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 19 May 2026 23:23:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:23:52 GMT
WORKDIR /root
# Tue, 19 May 2026 23:24:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=45773140810cfd433402a58bb2ead4f43cc55805c34d2de0641c51012591d65c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c8919bba2fa9f72801d709485fcff27f73f0cc58d3f3f5dd056a44a317848ffc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17e901b9029c1be256c64d937595725a242b2052dab810d7d10f715bed7b6d90;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f603a24bdaa9fc31c498c558bfeed8e3ebab84c0e085974eb5849c1cec756b3e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1b1ae8a7e42806901c304c81a9efa987576c8e3ceb606248b87873e1bbb3be`  
		Last Modified: Tue, 19 May 2026 23:24:36 GMT  
		Size: 42.5 MB (42504590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09d6b94bf9854ce098e9fe04fa1b325b725582f6fbe640d870176a3177d39d4`  
		Last Modified: Tue, 19 May 2026 23:24:34 GMT  
		Size: 1.9 MB (1869788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a444e4d66d3c4b158f39baef6921755c222c9d6b9d3c6af623f1c05cb0294a`  
		Last Modified: Tue, 19 May 2026 23:24:40 GMT  
		Size: 236.8 MB (236792307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6caef5f66b5f6f285c18711b9f3af3f32d052bf52db724040c8d11a090804351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63781ade8c4bd9cc4556b01f23669e75df6079a77f3232beff87a562eedbe929`

```dockerfile
```

-	Layers:
	-	`sha256:5ede8138b079248fb9cd6cca4e7f68bc64d5ab2418c9e1e6db7c4c0697a7695a`  
		Last Modified: Tue, 19 May 2026 23:24:34 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:0a18b7ba9489d390854e6266a22d3fd4d68444afc556bf4909a69d3a36a64382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226071496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6dd58dd8542bc6fb60f28a71886db1327a756f5768da78476745fae3be0031b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:07:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:07:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 May 2026 00:07:51 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 May 2026 00:07:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:07:51 GMT
WORKDIR /root
# Wed, 20 May 2026 00:08:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=45773140810cfd433402a58bb2ead4f43cc55805c34d2de0641c51012591d65c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c8919bba2fa9f72801d709485fcff27f73f0cc58d3f3f5dd056a44a317848ffc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17e901b9029c1be256c64d937595725a242b2052dab810d7d10f715bed7b6d90;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f603a24bdaa9fc31c498c558bfeed8e3ebab84c0e085974eb5849c1cec756b3e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcb232070ef0f1260ca1db8ab9faa9460c3544d787e0fd6f8708f5e0be4a2f5`  
		Last Modified: Wed, 20 May 2026 00:08:21 GMT  
		Size: 37.5 MB (37502823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e397e0cd660862cdbd2e6a3cdbc97550fa640df55588d7f35c0b0afe9085bf`  
		Last Modified: Wed, 20 May 2026 00:08:20 GMT  
		Size: 1.3 MB (1273147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9dc45c8ea6119a7a402db2df614758a88a42298a95511f579aab39d651de13`  
		Last Modified: Wed, 20 May 2026 00:08:24 GMT  
		Size: 161.1 MB (161089663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1f49a2e34265a115761248f7604e59ad5fed9ca3717d39eea241138b91e06571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b52997781094e317c304d1ef3d8cbf3b2722c85c8de3166261cf4c2df195b1`

```dockerfile
```

-	Layers:
	-	`sha256:63a96dcfa9fc9461f5d568481ff235b882cdf13323c49fa5c2a627a8526f7ae5`  
		Last Modified: Wed, 20 May 2026 00:08:20 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d729f80447785f1f894f8a53e1cdbcc48f4f4f466e309080516898fd2f1cd2c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309397260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f319fcb7f747aeea30d2e2b194f8ac264abc8d3de4965225823681f639307767`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 19 May 2026 23:27:33 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 19 May 2026 23:27:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:27:33 GMT
WORKDIR /root
# Tue, 19 May 2026 23:27:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=45773140810cfd433402a58bb2ead4f43cc55805c34d2de0641c51012591d65c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c8919bba2fa9f72801d709485fcff27f73f0cc58d3f3f5dd056a44a317848ffc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17e901b9029c1be256c64d937595725a242b2052dab810d7d10f715bed7b6d90;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f603a24bdaa9fc31c498c558bfeed8e3ebab84c0e085974eb5849c1cec756b3e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3645a37f8fc09cecc135c9364ddc54c40258ecc0952a4b1aeaf132334a8d9499`  
		Last Modified: Tue, 19 May 2026 23:28:17 GMT  
		Size: 42.3 MB (42285546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364ff266e460e8fbc72a711448b062b61b92c08f3ba4c707d95b48e48910aca5`  
		Last Modified: Tue, 19 May 2026 23:28:15 GMT  
		Size: 1.6 MB (1564373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf6e9b9989e2b80548dd02c59319a245a85992d8018c2b44f370e0f2e73ae60`  
		Last Modified: Tue, 19 May 2026 23:28:21 GMT  
		Size: 235.4 MB (235405390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:9d16af0994ab8e6e73274caa2d49ab9a1095a1a002854a3c4b9d3b5d2d2bd178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afe7e0c5e20589dfa43acae202acbddc969119d7df73974090cadc7e044bb49`

```dockerfile
```

-	Layers:
	-	`sha256:1d137efcd85714ccce7d9c28c75032ab9626b918bc2e25535173bc9dab64b607`  
		Last Modified: Tue, 19 May 2026 23:28:15 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:c0eb5fa688f5525ff5df8dbc63749da3b1c4d25912c789a7c5c4f53cbacafb97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.0 MB (250950023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1540c91d223c38a121e014884360b800cefb36bb4a3f87e4cb576eab9583d43d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Mon, 18 May 2026 22:04:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 May 2026 22:04:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 18 May 2026 22:04:58 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 18 May 2026 22:04:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 May 2026 22:04:58 GMT
WORKDIR /root
# Mon, 18 May 2026 22:05:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=45773140810cfd433402a58bb2ead4f43cc55805c34d2de0641c51012591d65c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c8919bba2fa9f72801d709485fcff27f73f0cc58d3f3f5dd056a44a317848ffc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17e901b9029c1be256c64d937595725a242b2052dab810d7d10f715bed7b6d90;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f603a24bdaa9fc31c498c558bfeed8e3ebab84c0e085974eb5849c1cec756b3e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df7a545a9c9ac31e2f10cd3db88e43d767dd05641bb5163e43666ef844f5d54`  
		Last Modified: Mon, 18 May 2026 22:10:01 GMT  
		Size: 44.2 MB (44197224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a6067d7809cbf30db431cbbd98ba1012062dc51068ea326bd973badb7d544a`  
		Last Modified: Mon, 18 May 2026 22:09:48 GMT  
		Size: 1.6 MB (1564400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d721e4e75a2cf62cd3f18071616671a36d8f65322f3e18d237b040f009692ff`  
		Last Modified: Mon, 18 May 2026 22:10:21 GMT  
		Size: 176.9 MB (176908135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:054022df4c7230c0a7927ba3ca6cac93c13afd1508ebe6c1409b4b3bbc7fe9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d0c929324371414bdfdc944b526c3b2d333a65fe3e2ba49a5eae84e693ccbf`

```dockerfile
```

-	Layers:
	-	`sha256:780e6ac836774b1e3504b87051e9678317199cb5216c0452ed6a44ee4ce58fa6`  
		Last Modified: Mon, 18 May 2026 22:09:47 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json
