## `dart:beta`

```console
$ docker pull dart@sha256:0d1eae0d64f8fd7c316a398344773d219439bfa5479134764215b52b6bd19915
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

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:17da6dbfdc92c173356c22ff596ad00ba27980c9ca3f1a417b5d6cc85f6548f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.9 MB (313904716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8d5724d0acd0267aced860a44466d7f8ae00a9a2ed64df7b60c86ae280639b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 21 Apr 2026 17:13:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 17:13:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 21 Apr 2026 17:13:39 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Apr 2026 17:13:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 17:13:39 GMT
WORKDIR /root
# Tue, 21 Apr 2026 17:13:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=60484d3bb620de44f11b0078571f288fe1b5c6207369e4a5a92a0d942fe183d7;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bd92bd905c5208ce6b7063db7a820ae78d90b9d4c0b6a9d1091e794a93721d8d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1053dde7acf75a594b81f1612e7eab427a62b69f73339667b87f6224e705e695;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=90eafc92bc56cc141462cae7aef2ce02bcc1a0111e68be67bc188cf695fbf46b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04b5a94a22802dd228189a5d3ff92043138aba46ef078f063c2120d6336a441`  
		Last Modified: Tue, 21 Apr 2026 17:14:20 GMT  
		Size: 45.5 MB (45466165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16070a2c9768719bf70a1ad8270798952e7ecacc5d4a21e3ce56d8d0abc78b5`  
		Last Modified: Tue, 21 Apr 2026 17:14:17 GMT  
		Size: 1.9 MB (1869572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffaa211f27056c97e3aaa992c0a6a722f5f56d936166ba47a22a1329a81fe94f`  
		Last Modified: Tue, 21 Apr 2026 17:14:23 GMT  
		Size: 236.8 MB (236793307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:8cf97a2aa65fc9df2c2d75fc59c5f4f7dfd62a3accd07bc67cf09ef74392ffa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b767eae9afb7b18032f6257b5cc2e63b92c660c8996ef8f4369c752a8ae30f5`

```dockerfile
```

-	Layers:
	-	`sha256:d55418e4bb6708aca3ceeed4725974b330819e060ebb001451eba06582de86da`  
		Last Modified: Tue, 21 Apr 2026 17:14:17 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:72939d508f8e07dbc86e4e4b3128a01bcf4d1ecd2848e22a23e62cfb37df8dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228282449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4c0073c037b230cdc6640c73b73d688234357f6d51c72aa5a2e38ec886a17f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 21 Apr 2026 17:11:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 17:11:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 21 Apr 2026 17:11:40 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Apr 2026 17:11:40 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 17:11:40 GMT
WORKDIR /root
# Tue, 21 Apr 2026 17:11:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=60484d3bb620de44f11b0078571f288fe1b5c6207369e4a5a92a0d942fe183d7;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bd92bd905c5208ce6b7063db7a820ae78d90b9d4c0b6a9d1091e794a93721d8d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1053dde7acf75a594b81f1612e7eab427a62b69f73339667b87f6224e705e695;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=90eafc92bc56cc141462cae7aef2ce02bcc1a0111e68be67bc188cf695fbf46b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1126e43411edf0a289426ef6b6e3ed3e0e553528ab6e158b9448106fe388d149`  
		Last Modified: Tue, 21 Apr 2026 17:12:13 GMT  
		Size: 39.7 MB (39713186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6460b1a543dee136fc0f17920f304016ad8850cd982a26eec9c1700c4c495984`  
		Last Modified: Tue, 21 Apr 2026 17:12:11 GMT  
		Size: 1.3 MB (1273172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4ef0e4ccb3892b5f3e1e61175f3dc03944278ca907348d3d8af47fb26c3f69`  
		Last Modified: Tue, 21 Apr 2026 17:12:15 GMT  
		Size: 161.1 MB (161086406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:f3935f8cc7f18ca62301da87c8cfecea986f860ea1035b96c32b3cf5bd063ab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04919c3a33d7a997cc943f4ccee65d359654733c3f4004822a6403e485129c4f`

```dockerfile
```

-	Layers:
	-	`sha256:fa8aac247fdc876afa463ed860e9117c2367a88f566246f2f857c7332604b340`  
		Last Modified: Tue, 21 Apr 2026 17:12:11 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:111bf759e89c6759188a5da873fcba5982d2badd4e595ed5113d477e0395efda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312712628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4fdaa9e03537408944e2b457ab7b4982aff1e587902a83352e0fb2de10841e1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 21 Apr 2026 17:13:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 17:13:41 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 21 Apr 2026 17:13:41 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Apr 2026 17:13:41 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 17:13:41 GMT
WORKDIR /root
# Tue, 21 Apr 2026 17:13:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=60484d3bb620de44f11b0078571f288fe1b5c6207369e4a5a92a0d942fe183d7;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bd92bd905c5208ce6b7063db7a820ae78d90b9d4c0b6a9d1091e794a93721d8d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1053dde7acf75a594b81f1612e7eab427a62b69f73339667b87f6224e705e695;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=90eafc92bc56cc141462cae7aef2ce02bcc1a0111e68be67bc188cf695fbf46b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f66366cff512c2e4cfae2e12d2c1582d38739a0bb4e38bd3a117038579cc6e0`  
		Last Modified: Tue, 21 Apr 2026 17:14:25 GMT  
		Size: 45.6 MB (45616363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0c476b0d14a4f3ac503c4634164961865f7a9bde99e8e81ca65caddc17e007`  
		Last Modified: Tue, 21 Apr 2026 17:14:24 GMT  
		Size: 1.6 MB (1564345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6039a92932e9e214ad5b546eee332631e38e5fbded972731200f1fddf8fdcfe2`  
		Last Modified: Tue, 21 Apr 2026 17:14:30 GMT  
		Size: 235.4 MB (235393337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:5d107c546c07d6ed7d5bf9d31e84fde71ede0fc9f7517501bd45974df1676245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3737262a95b043bc0051d6a8fcacd0b8c0f5ceb7e6477f28d9a48be5ea72c764`

```dockerfile
```

-	Layers:
	-	`sha256:2cea7dc1df0bcddb84931049dab948242a80b41ca7d7d58dd3f1dcc186b4020d`  
		Last Modified: Tue, 21 Apr 2026 17:14:23 GMT  
		Size: 19.1 KB (19056 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:bd4db99b405505a9d0a4abc7913602368c005a5ecf8458e8a4a5624123e22552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250940694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86537e85f22ee58b5e16bef83f8018a8c287fdba29dd27178ef37a531fdf5525`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 17:55:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 17:55:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 15 Apr 2026 17:55:21 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 15 Apr 2026 17:55:21 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 17:55:21 GMT
WORKDIR /root
# Wed, 15 Apr 2026 17:56:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=64567d16674aa558a059d3c1af2dcde5fe222e166d092b11a721285d41361679;             SDK_ARCH="x64";;         armhf)             DART_SHA256=df9611c016da694f1d36dd923fc392bb1d5f9b3b5b8bf93d2367afdeb8522908;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e211c35ce943eea9f2038c0ef351bad325ba959d7c58cf4e77f6eacc02389459;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=a0b2e7509e369ffb8f531526f7fb60003fda4bbee0da938fafa282d5c6e78c53;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f5b5825255a5d4ee29acec2738aa43805937d5cf188e73592372b8d8cd778f`  
		Last Modified: Wed, 15 Apr 2026 18:00:44 GMT  
		Size: 44.2 MB (44183572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba610148dc501ed1a6c0cc789285e829e79332eb3ddd25d785e76a09e6cd77b`  
		Last Modified: Wed, 15 Apr 2026 18:00:28 GMT  
		Size: 1.6 MB (1564396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2a91fd004f5730e04f28e3f19160543f5342a0e99410bdc189d9c65fb41c95`  
		Last Modified: Wed, 15 Apr 2026 18:01:00 GMT  
		Size: 176.9 MB (176916916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:8393688d7ac3395727e60174421289ec1108ee287c6ada016fe293f3805cb6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac945532d73e38fa6e58772ac4cb9a7baf47991fec39577c1451486ff65e08f7`

```dockerfile
```

-	Layers:
	-	`sha256:3809ff7bb5df0f204db71804d6c735e90225e68b0ee3aa216b98a69c081c1daa`  
		Last Modified: Wed, 15 Apr 2026 18:00:28 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json
