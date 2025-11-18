## `dart:latest`

```console
$ docker pull dart@sha256:78ec6a5fd1834ad0f5816e314ef8ca2abbf49c1fb8b9019ee5ba69890435110f
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
$ docker pull dart@sha256:844bfd1345200e1bf8569cf126cc33cf49a68c9d4eeb3f5786b473462f9457e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287266367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10489852d91ace3839022540130b2fc4b236784611337c7d0aea708ff6e5130`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:14:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:14:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 05:14:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 05:14:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:14:13 GMT
WORKDIR /root
# Tue, 18 Nov 2025 05:14:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a27681be873c3891692285db8d656e7494ca80c74e86613b8085fc6cffa3e31d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b91536edbcafc0d6389b8db6d1677bac0c608a1578fdf7c919b47b439aa044f1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=688603283b9a9e7833da53eb5b3a07d78fea9c51fdd925bbfd922775d4ba5ea3;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dafc564768e0063170e5f0c663b90c3b4570ad3cd39c9bff3790f03e6b8554bb;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f8b3aab59b23b21dc316ff8a64ac586bb26f94d06e6e67eabfb37f42f08bb0`  
		Last Modified: Tue, 18 Nov 2025 05:15:11 GMT  
		Size: 42.5 MB (42494004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd7146c2ff3af70c36973e9afcdb90cedbce63fe168664a2716cfc5d7008de8`  
		Last Modified: Tue, 18 Nov 2025 05:15:06 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd962cd70cbf47d54f4a08c6eb7a5233916ad5b85fea142b52fd87d1d49df40c`  
		Last Modified: Tue, 18 Nov 2025 06:54:40 GMT  
		Size: 213.1 MB (213122229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:bed40df503b29500cbc058eaa619feb8c44a768cda2321593777993763628e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7de61e0bdfebe9a1513cd91ff0c38797fcadc866de4a6096000c1ee6fc2685d`

```dockerfile
```

-	Layers:
	-	`sha256:eefe035387b3b5baecc7c3311c13b71628140447520be7fa876d54e124a7043b`  
		Last Modified: Tue, 18 Nov 2025 06:54:03 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:99961058dbb76034b85c65ece56ff2773b6301add6fc5c61e3f567e39af549b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219896782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3224ef068eafbb4930e6fedc27fe8552feb893b19e36b80e7d0900dcfb546c0b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 04:18:56 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 04:18:56 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:18:56 GMT
WORKDIR /root
# Tue, 18 Nov 2025 04:19:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a27681be873c3891692285db8d656e7494ca80c74e86613b8085fc6cffa3e31d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b91536edbcafc0d6389b8db6d1677bac0c608a1578fdf7c919b47b439aa044f1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=688603283b9a9e7833da53eb5b3a07d78fea9c51fdd925bbfd922775d4ba5ea3;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dafc564768e0063170e5f0c663b90c3b4570ad3cd39c9bff3790f03e6b8554bb;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e284bf5577f4b195a3a38ba8e2ad1b5af5b7fe861b229c2f3f6a02b8acc33ce4`  
		Last Modified: Tue, 18 Nov 2025 04:19:37 GMT  
		Size: 37.5 MB (37498304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6fba1ba02ba360efce1a0302230cadbadf791d5d212fcb9a1a952b554c57d5`  
		Last Modified: Tue, 18 Nov 2025 04:19:35 GMT  
		Size: 1.3 MB (1275123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ff57fe8540a9e7cf890cd449c044e75b337cb6b31152c2dd70ce3830817bce`  
		Last Modified: Tue, 18 Nov 2025 06:54:31 GMT  
		Size: 154.9 MB (154913363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:d524c5407bbb88056826a196c1630654ebe1f7d97df7c6ea245c699651e9986f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d913b30e30d2f670db945ad42a9db2c7983cf8c9e1e206b44cdc029cfeda48d`

```dockerfile
```

-	Layers:
	-	`sha256:e81c84ba2e8318d819f99102fa8848b0c1468c15fa3426c1ba9abe13d5577873`  
		Last Modified: Tue, 18 Nov 2025 06:54:06 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:2381424cdb6a7e84a7015b616f35ce795f68d8947c384bb29b76131a91846d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286355032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f382da7f57735a2648795cfac93d66c5b78b139890bc2bf3aaefc447d8d6e6a5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:36:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:36:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 03:36:31 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 03:36:31 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:36:31 GMT
WORKDIR /root
# Tue, 18 Nov 2025 03:36:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a27681be873c3891692285db8d656e7494ca80c74e86613b8085fc6cffa3e31d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b91536edbcafc0d6389b8db6d1677bac0c608a1578fdf7c919b47b439aa044f1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=688603283b9a9e7833da53eb5b3a07d78fea9c51fdd925bbfd922775d4ba5ea3;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dafc564768e0063170e5f0c663b90c3b4570ad3cd39c9bff3790f03e6b8554bb;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d00149698c24851b9b2a6acc7a54a3cd45b38f13ffddc271e6e001a2fced914`  
		Last Modified: Tue, 18 Nov 2025 03:37:24 GMT  
		Size: 42.3 MB (42293016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5dcfe009c746e3330bf3254252af45bd2369e47acd5f30fa33096fe0d02161`  
		Last Modified: Tue, 18 Nov 2025 03:37:21 GMT  
		Size: 1.6 MB (1566643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2410a0d982622e4cefa8a3b7ac77d2ac3e2b4e528305c3dc3e5decd9e554df8d`  
		Last Modified: Tue, 18 Nov 2025 04:34:43 GMT  
		Size: 212.4 MB (212356731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:0f55563714f66fee436a86c330a3c8407f2e9fc41baaf8a062522d28c91f9470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febefe8b2f79affcaf3538d98ad6ecdd69a471fbe900442971d6d71b92c3cef6`

```dockerfile
```

-	Layers:
	-	`sha256:8c86c1ad8c222d6d01563de280c22c5b895524237c995e39d8efebccb5f053ac`  
		Last Modified: Tue, 18 Nov 2025 06:54:09 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; riscv64

```console
$ docker pull dart@sha256:4ac279a2751c8d947d868ac3335a8fbefedc3a9cc17c6fab6dd8ea62e1698286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232961159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e2764ca25e8de968c19022475a973ae0845551de212386a9ab669aeeb9614e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 11 Nov 2025 22:16:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 22:16:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 11 Nov 2025 22:16:04 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 11 Nov 2025 22:16:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 22:16:04 GMT
WORKDIR /root
# Wed, 12 Nov 2025 18:34:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a27681be873c3891692285db8d656e7494ca80c74e86613b8085fc6cffa3e31d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b91536edbcafc0d6389b8db6d1677bac0c608a1578fdf7c919b47b439aa044f1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=688603283b9a9e7833da53eb5b3a07d78fea9c51fdd925bbfd922775d4ba5ea3;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dafc564768e0063170e5f0c663b90c3b4570ad3cd39c9bff3790f03e6b8554bb;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c197f3fb63a08d839b0be1ce3d42db3af7f54f27346b95f111b82b21cc267fa8`  
		Last Modified: Tue, 11 Nov 2025 22:21:21 GMT  
		Size: 41.6 MB (41560559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80bf767ca6af272d9eb378bc7d2f7a727579f404cc0d6158b26873863458f082`  
		Last Modified: Tue, 11 Nov 2025 22:21:09 GMT  
		Size: 1.6 MB (1567072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8910b20a5b61a5e6eb5fbdf416c103ad9f4ba71a2d492de86aecf1952e38c7ad`  
		Last Modified: Wed, 12 Nov 2025 21:53:58 GMT  
		Size: 161.6 MB (161557710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:9d266cc2175f1dd491a9e52189c7993d30e0866e2afa05e5a06fc156a8191fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281494f65aca1381b8ed9cefd381f6f5226df7333ebbb611de8fdd8860ee46e9`

```dockerfile
```

-	Layers:
	-	`sha256:26d3f6dbf672ab11fb368f2ffdb421f3f318512ef6ca6908d8eda182a3a94f2c`  
		Last Modified: Wed, 12 Nov 2025 21:53:29 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json
