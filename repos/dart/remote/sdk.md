## `dart:sdk`

```console
$ docker pull dart@sha256:80a71960b42a8fe5fbc9756c46ba0e773a1b1e604ab30bd42ccf50c906c6cabf
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

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:694cae58388079971a64f07258f719a2d8a8dcce42e6581b37a155ce852f2dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.0 MB (310953113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677d0c32b2c0e4dc90cf3405e4cee0d0493959ce742d8ef3b582fafcf7760ee2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:42:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:26 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 24 Jun 2026 01:42:26 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 24 Jun 2026 01:42:26 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:42:26 GMT
WORKDIR /root
# Wed, 24 Jun 2026 01:42:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=28e47b44cf075f36771046c068bb0d174201cf9c7608744aed1cc23204299c2d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=659fd41329db2c17e5f186c351fff50ac026b0ed1770a6ace712364d309b4a39;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f82c83ece7d168047550dfd4a664e4071ac7c488bddb72dc43102c22d7e0b518;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c11cf4764fabac705118c02fc4ee3bf3b7210ac6919329ead8ceed5cf63a4820;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546f06f2447b2104c02fc18406ab9c75393c903de17461b5f1e91d86611e9abd`  
		Last Modified: Wed, 24 Jun 2026 01:43:09 GMT  
		Size: 42.5 MB (42504482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76277b39b379866ab1562305eb7e4a4aef65db57bc879adf393aa3de3b752560`  
		Last Modified: Wed, 24 Jun 2026 01:43:07 GMT  
		Size: 1.9 MB (1869785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349b63ee237e7b69b6ef7e72dc457eed748db83fd06ba0db06f195bffd8f9971`  
		Last Modified: Wed, 24 Jun 2026 01:43:13 GMT  
		Size: 236.8 MB (236793395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c0d33d664d0e254ce9fb5b2bd1b8a79ae6c2284f8b99d5db1032297418dba0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c3d73029403f97c11bd220cc6287195824c0b2a484b3950ee1b682949d8b94`

```dockerfile
```

-	Layers:
	-	`sha256:bc3d48a3d193472d2ce1f487f4a498795270a859b1246bb8d44f31e312873cf6`  
		Last Modified: Wed, 24 Jun 2026 01:43:07 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:97820044ca019719f6cbce8a2c6dd952233e72990193548afa0cd4ae32127351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226079743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12912f78e05155f4bb30799c0b5efcb355ceac3c39675f56d6dc49ca305b602d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:29:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:29:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 24 Jun 2026 02:29:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 24 Jun 2026 02:29:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:29:38 GMT
WORKDIR /root
# Wed, 24 Jun 2026 02:29:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=28e47b44cf075f36771046c068bb0d174201cf9c7608744aed1cc23204299c2d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=659fd41329db2c17e5f186c351fff50ac026b0ed1770a6ace712364d309b4a39;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f82c83ece7d168047550dfd4a664e4071ac7c488bddb72dc43102c22d7e0b518;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c11cf4764fabac705118c02fc4ee3bf3b7210ac6919329ead8ceed5cf63a4820;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:81c84b0273952340067af970e1fe77a42ea83b4ed1a53319e258d5f1077848f0`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 26.2 MB (26211051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b9a23d7aa1cc19100ee4f3176287431e51904a13f5b630d8323ba742c2e0d7`  
		Last Modified: Wed, 24 Jun 2026 02:30:08 GMT  
		Size: 37.5 MB (37509600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b63c4dbd10d63f5353831579e72d267b1615b44e377d66d806ce51d7a1796fe`  
		Last Modified: Wed, 24 Jun 2026 02:30:06 GMT  
		Size: 1.3 MB (1273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a41881b20781167c38993c050d0322ea7eeffa324f55b211f29d3e9c155a3e2`  
		Last Modified: Wed, 24 Jun 2026 02:30:12 GMT  
		Size: 161.1 MB (161085904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:f759af22e436ac5a82a3935b810162328b7fbf242b9e55185b25ee40cdf1e84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b67a3092e62925ab54e5a7f3bf7e79d8f7b6f6275b41b7c3426806c17969962`

```dockerfile
```

-	Layers:
	-	`sha256:8bfaff2915ca48012f3a74973a4d99e3889c4af1cb562f1d6a8888af9e95d5c5`  
		Last Modified: Wed, 24 Jun 2026 02:30:06 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:976d66148024133f722d0705a917f4e11e4f9d3e8054b16373e2fa7d4fadbada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309403851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9e53e7063a5bc7d9a0be50418baaf8fa4feaecfceee2a3983b9ce35f243efe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:45:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 24 Jun 2026 01:45:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 24 Jun 2026 01:45:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:45:45 GMT
WORKDIR /root
# Wed, 24 Jun 2026 01:45:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=28e47b44cf075f36771046c068bb0d174201cf9c7608744aed1cc23204299c2d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=659fd41329db2c17e5f186c351fff50ac026b0ed1770a6ace712364d309b4a39;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f82c83ece7d168047550dfd4a664e4071ac7c488bddb72dc43102c22d7e0b518;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c11cf4764fabac705118c02fc4ee3bf3b7210ac6919329ead8ceed5cf63a4820;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396bb34eedde8676b08722072913cb0e3b97eeba65328509cde1fee86924e744`  
		Last Modified: Wed, 24 Jun 2026 01:46:24 GMT  
		Size: 42.3 MB (42285684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402fc6b0db72064ba14f8c5b418b03506f0b0456fff4282377601cdd68fb2905`  
		Last Modified: Wed, 24 Jun 2026 01:46:22 GMT  
		Size: 1.6 MB (1564374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb213532b6bfc5815894608f4c783af13a67536d9d2c5f8f297cc165d7018b2`  
		Last Modified: Wed, 24 Jun 2026 01:46:29 GMT  
		Size: 235.4 MB (235405210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:653c2594cc3ad01e89d03a58a881fedf39fa66517f881af0e846825ae0045f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17c3c22129dd2e6d53c3e47e153f05b29d40d631e380ed6baea521feac23f5a`

```dockerfile
```

-	Layers:
	-	`sha256:7166e9955bd1e297648042ab0ed3282580fbe222c70d85040832bb68e501dc2f`  
		Last Modified: Wed, 24 Jun 2026 01:46:22 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; riscv64

```console
$ docker pull dart@sha256:72f7705d1143c854b016a038f0a659c36d7ca3b5ae3459468380bd2d0df7dd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.3 MB (248337423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c35bf942335764a434d698f12624ffb0b7b4e81f549dffa293c75db1645a6df`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Sat, 13 Jun 2026 04:48:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 13 Jun 2026 04:48:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Sat, 13 Jun 2026 04:48:32 GMT
ENV DART_SDK=/usr/lib/dart
# Sat, 13 Jun 2026 04:48:32 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jun 2026 04:48:32 GMT
WORKDIR /root
# Sat, 13 Jun 2026 04:49:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=28e47b44cf075f36771046c068bb0d174201cf9c7608744aed1cc23204299c2d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=659fd41329db2c17e5f186c351fff50ac026b0ed1770a6ace712364d309b4a39;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f82c83ece7d168047550dfd4a664e4071ac7c488bddb72dc43102c22d7e0b518;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c11cf4764fabac705118c02fc4ee3bf3b7210ac6919329ead8ceed5cf63a4820;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6be4cefd7f65f65198a30dc6ce75840f49972ba95c99f94b1f1e3b1d8a236f1`  
		Last Modified: Sat, 13 Jun 2026 04:53:38 GMT  
		Size: 41.6 MB (41577683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd053d4c11b60ee6c96c89922f75d3bcc6071ffe5404a606a624413278acb483`  
		Last Modified: Sat, 13 Jun 2026 04:53:26 GMT  
		Size: 1.6 MB (1564448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5046ba704fa9e9a4f0e2891961c50c86faca6471bfbdf17869dcc1d949ec9eb4`  
		Last Modified: Sat, 13 Jun 2026 04:53:59 GMT  
		Size: 176.9 MB (176912955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:33d3bfa7716487d84f5dc63a4e47c1928d3267025c822f16cdc222176ec20f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295d9d324fa45ec422d046b1c9f1387119d5cda416185df4f941912726652fa6`

```dockerfile
```

-	Layers:
	-	`sha256:e71f67d84d763fc8d25ab7a423c5776d1d20904fbb735a8ccd7d4db3c5bc3d8e`  
		Last Modified: Sat, 13 Jun 2026 04:53:26 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json
