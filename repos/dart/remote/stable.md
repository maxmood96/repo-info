## `dart:stable`

```console
$ docker pull dart@sha256:6440c7d5fd8713b0706d0b6190eb2be7ad896101e225fc9d7657034b23ab0592
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

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:1084929f4e943f44fd86c78500d22a4339469354a374574ecc16a2aabfd2582f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310942915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee2b2dbfbebaf4146fd0560471ee6229ec6ae294c9fcaf2776f4a8eadfa8abc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:31:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:31:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:31:56 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:31:56 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:31:56 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f61b2fe77f050f4ca332791e970839ee640079b59c7b53688e1f1b57aeac212`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 42.5 MB (42504481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02046203169b09dd439aee7573065dfeb9a315df8eca955bff762a861c854aff`  
		Last Modified: Tue, 26 May 2026 20:32:33 GMT  
		Size: 1.9 MB (1869790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c4abf572584d12407b08706626e143ff8cfcb141cd72bb0944c0e11ff83e5d`  
		Last Modified: Tue, 26 May 2026 20:32:46 GMT  
		Size: 236.8 MB (236788686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:7662ef2d512115d6ef2963f51fd168a2432dd186dbe29e3347d47436386cf536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd66ca8e1d5016f2aea61a8dd844f5335c777dad65f65582a625d53c6c8308f1`

```dockerfile
```

-	Layers:
	-	`sha256:63c6e102192cb2c8676951b6a7cdf6229f35712d9e7412245f8b838bf6269169`  
		Last Modified: Tue, 26 May 2026 20:32:33 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:f04de8d20306fec21c148ae2fa0ebdf6da6a379262d97dafa0a7b4bb7178728b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226078344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e3dc4d47e77fb089b94f285993f313895b52ac9b8570ab2c18667941173586`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:32:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:32:05 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:32:05 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d27d7a75151cc5bd699515a5d3097fd940446c299f659e359320f74e5ce9c9`  
		Last Modified: Tue, 26 May 2026 20:32:38 GMT  
		Size: 37.5 MB (37509460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488f84b526710261b0936f6401897f0144cdcd34a3152f8c629f7ad190e80d2`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e32f7c39bac5379adb0c968d408e5921141b187eb329acb8752ba34728fe709`  
		Last Modified: Tue, 26 May 2026 20:32:41 GMT  
		Size: 161.1 MB (161089868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:e16e1be8c8d332c96675d3d53627af6df60592752947823f856bd0e871779143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d0f80676ce4d8d3bc881c4b95a688fdf49ef49e8bc528e1733113dae35bac5`

```dockerfile
```

-	Layers:
	-	`sha256:902d802aafa445250a18077914d1985faae10f00b37d254b4af45019d7bfe5cf`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:df748054c761938f24bae1e3876b0a29dc0b7cfaecbb0dd0883af5d2c3c076a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309389795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c238a332a84f01dffc64a14ac91694e533232fb9f949b3d5229d8d4442a7941`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:31:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:31:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:31:52 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:31:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:31:52 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff8a7689f6c9f14c0653099d5e198fe1a17373899dc456f3f7a333959498a3d`  
		Last Modified: Tue, 26 May 2026 20:32:37 GMT  
		Size: 42.3 MB (42285764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937db8af4819e606d38a27f0917ff9a96fc90950463b7b8e43a11c907fd734d1`  
		Last Modified: Tue, 26 May 2026 20:32:35 GMT  
		Size: 1.6 MB (1564378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f2479714efd63130d273102cb8377f276edbc3e9bd8bd0aa7676c2784a7a9`  
		Last Modified: Tue, 26 May 2026 20:32:44 GMT  
		Size: 235.4 MB (235397702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:5a848294cf6b9099bf97bd50aa7f591d0ae8d47616dc98c907b1df1c1f8f3bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3515f2b37b72250729227324cec1092d27e673f5674e6f836b942140a267119`

```dockerfile
```

-	Layers:
	-	`sha256:1290ad536f1527c5745bdce044ebf1deaaf3ee5433e731589eec822827fd26f9`  
		Last Modified: Tue, 26 May 2026 20:32:34 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; riscv64

```console
$ docker pull dart@sha256:59841369e27e87cfdf3ea756dc55ab177ff5c3c45dc78589ad583a7ebbef5d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.3 MB (248328469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28932dd8174e7b39d8238c4d940518499dde72eba16661cdafe5b884bd9cf404`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Wed, 27 May 2026 21:44:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 May 2026 21:44:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 27 May 2026 21:44:43 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 27 May 2026 21:44:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 21:44:43 GMT
WORKDIR /root
# Wed, 27 May 2026 21:45:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cfbf3292df36b0557da9a4b4cd22aeff880e1e9bb6b55aff6dabf41a3e1eb6`  
		Last Modified: Wed, 27 May 2026 21:49:55 GMT  
		Size: 41.6 MB (41577865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904241ccc7375627a755ff0c7ba8b91ea0b5e559cdbe38e37909283a18525ff0`  
		Last Modified: Wed, 27 May 2026 21:49:43 GMT  
		Size: 1.6 MB (1564446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa8720274d8f3bfaff9d93de2b9ae69920fd94d74bb4fbe4ef9a4973cd777c8`  
		Last Modified: Wed, 27 May 2026 21:50:15 GMT  
		Size: 176.9 MB (176908528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:c9e03d1e6250a08282b9cd4e8ce788e49d040453c634c78cde0f604d697b2543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda39fee2234cf6d2439030b52cd04549d61b8e73f1cf63a2b8ecb00f077b850`

```dockerfile
```

-	Layers:
	-	`sha256:d1b3f027c86b12b00164a35ca57eae5a6c0064d7a996f63693ede383d0c77140`  
		Last Modified: Wed, 27 May 2026 21:49:43 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json
