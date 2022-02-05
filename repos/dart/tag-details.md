<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:2`](#dart2)
-	[`dart:2-sdk`](#dart2-sdk)
-	[`dart:2.16`](#dart216)
-	[`dart:2.16-sdk`](#dart216-sdk)
-	[`dart:2.16.0`](#dart2160)
-	[`dart:2.16.0-sdk`](#dart2160-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:2`

```console
$ docker pull dart@sha256:929127073796cc98376c5cad4633bf2031e4d4f1261dba33b3d65ade4a914d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2` - linux; amd64

```console
$ docker pull dart@sha256:5615d36ab612eb6edb43f1d6e594c6bf5d4e6f0f83bbb06ddb1ef0822122f69d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280118262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff28224215fa6f9ef187fc0c8a3260a02e1f0f07b834b6502c13c267f27df78`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:35:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:35:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:35:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:35:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:35:56 GMT
WORKDIR /root
# Fri, 04 Feb 2022 21:24:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260f85c7c1aebd4382688a5dd10aa11a241660ea1420867bfa423146bb5e7cb1`  
		Last Modified: Wed, 26 Jan 2022 02:37:06 GMT  
		Size: 49.6 MB (49582700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90aea65c283280db5f2c3e5baf6f94dad74c4970a49c4b080c5ac92da97b09df`  
		Last Modified: Wed, 26 Jan 2022 02:36:55 GMT  
		Size: 2.4 MB (2359153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b3e35b79b51308e44a2c862fcdf7e0f3cfc5f1fc8dfb4bc1865ecc357841d9`  
		Last Modified: Fri, 04 Feb 2022 21:24:57 GMT  
		Size: 201.0 MB (201022678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2` - linux; arm variant v7

```console
$ docker pull dart@sha256:4dc621f597586d494e3c17cabf16cc81ada7d9fe9cd3a306fec9f37ddf04f13b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186695690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e74cbd7bc9da0eecf553b939f91f6a485476ca81041d0ef37912fe83089cfa1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:43:12 GMT
ADD file:ca8132e20773f7037458cc53fe20a7116f93c21c7479be5a2a1d739495dbe44e in / 
# Wed, 26 Jan 2022 01:43:13 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:25:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:25:00 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:25:01 GMT
WORKDIR /root
# Fri, 04 Feb 2022 21:41:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:20cc49690d9072283406c1c11e9b1dc1a247782cc8daa526b375d4a7f1cb6a94`  
		Last Modified: Wed, 26 Jan 2022 01:59:27 GMT  
		Size: 22.8 MB (22754397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9485b7f36107dac4417e8b7c0659296b3ad4a442719e4b2774a85d71ae3f97`  
		Last Modified: Wed, 26 Jan 2022 02:27:46 GMT  
		Size: 44.4 MB (44399462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19668bef3278d9adb593c7b8625c2956fcf32db075c16ae1fa0af31e948fcc0c`  
		Last Modified: Wed, 26 Jan 2022 02:27:25 GMT  
		Size: 1.4 MB (1355911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2534965437f2a04ef5d3694605b977cbf2ef2a46fe85480e2f7689e08817883d`  
		Last Modified: Fri, 04 Feb 2022 21:44:06 GMT  
		Size: 118.2 MB (118185920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f0bafd3720e9a797a3740e198ccf9663908253e97d097e44a06661d54ebb751c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196893761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91bb0b5e5082a0bb3112f6ec1dd45fd1aab7220c4a2660569b78fb153828041`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:56 GMT
ADD file:796bc43a948899ba53bddebf7f613769fe96e8ea3a27eb7143d079c7a166ab01 in / 
# Wed, 26 Jan 2022 01:42:57 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:37:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:37:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:37:43 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:37:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:37:45 GMT
WORKDIR /root
# Fri, 04 Feb 2022 22:02:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4c7c9f6f1115fd4f35807a2f6c1375759365a991748aee0111873e55255f150b`  
		Last Modified: Wed, 26 Jan 2022 01:49:55 GMT  
		Size: 25.9 MB (25923216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c695284c12e2e4760a2a37b71f9ed572a621c66646a8fb6336b0dcf6296b13a`  
		Last Modified: Wed, 26 Jan 2022 02:38:51 GMT  
		Size: 49.6 MB (49639076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd03d19014c31feceac42db72787ea78d0fd8a7ffc17bf99ed31807754b1c220`  
		Last Modified: Wed, 26 Jan 2022 02:38:44 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b182d756ce93dcd1597d6ec850f9945f3001407ef3a815a8b209b3b3c573db9`  
		Last Modified: Fri, 04 Feb 2022 22:03:39 GMT  
		Size: 119.7 MB (119699541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2-sdk`

```console
$ docker pull dart@sha256:929127073796cc98376c5cad4633bf2031e4d4f1261dba33b3d65ade4a914d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2-sdk` - linux; amd64

```console
$ docker pull dart@sha256:5615d36ab612eb6edb43f1d6e594c6bf5d4e6f0f83bbb06ddb1ef0822122f69d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280118262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff28224215fa6f9ef187fc0c8a3260a02e1f0f07b834b6502c13c267f27df78`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:35:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:35:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:35:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:35:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:35:56 GMT
WORKDIR /root
# Fri, 04 Feb 2022 21:24:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260f85c7c1aebd4382688a5dd10aa11a241660ea1420867bfa423146bb5e7cb1`  
		Last Modified: Wed, 26 Jan 2022 02:37:06 GMT  
		Size: 49.6 MB (49582700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90aea65c283280db5f2c3e5baf6f94dad74c4970a49c4b080c5ac92da97b09df`  
		Last Modified: Wed, 26 Jan 2022 02:36:55 GMT  
		Size: 2.4 MB (2359153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b3e35b79b51308e44a2c862fcdf7e0f3cfc5f1fc8dfb4bc1865ecc357841d9`  
		Last Modified: Fri, 04 Feb 2022 21:24:57 GMT  
		Size: 201.0 MB (201022678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:4dc621f597586d494e3c17cabf16cc81ada7d9fe9cd3a306fec9f37ddf04f13b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186695690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e74cbd7bc9da0eecf553b939f91f6a485476ca81041d0ef37912fe83089cfa1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:43:12 GMT
ADD file:ca8132e20773f7037458cc53fe20a7116f93c21c7479be5a2a1d739495dbe44e in / 
# Wed, 26 Jan 2022 01:43:13 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:25:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:25:00 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:25:01 GMT
WORKDIR /root
# Fri, 04 Feb 2022 21:41:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:20cc49690d9072283406c1c11e9b1dc1a247782cc8daa526b375d4a7f1cb6a94`  
		Last Modified: Wed, 26 Jan 2022 01:59:27 GMT  
		Size: 22.8 MB (22754397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9485b7f36107dac4417e8b7c0659296b3ad4a442719e4b2774a85d71ae3f97`  
		Last Modified: Wed, 26 Jan 2022 02:27:46 GMT  
		Size: 44.4 MB (44399462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19668bef3278d9adb593c7b8625c2956fcf32db075c16ae1fa0af31e948fcc0c`  
		Last Modified: Wed, 26 Jan 2022 02:27:25 GMT  
		Size: 1.4 MB (1355911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2534965437f2a04ef5d3694605b977cbf2ef2a46fe85480e2f7689e08817883d`  
		Last Modified: Fri, 04 Feb 2022 21:44:06 GMT  
		Size: 118.2 MB (118185920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f0bafd3720e9a797a3740e198ccf9663908253e97d097e44a06661d54ebb751c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196893761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91bb0b5e5082a0bb3112f6ec1dd45fd1aab7220c4a2660569b78fb153828041`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:56 GMT
ADD file:796bc43a948899ba53bddebf7f613769fe96e8ea3a27eb7143d079c7a166ab01 in / 
# Wed, 26 Jan 2022 01:42:57 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:37:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:37:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:37:43 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:37:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:37:45 GMT
WORKDIR /root
# Fri, 04 Feb 2022 22:02:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4c7c9f6f1115fd4f35807a2f6c1375759365a991748aee0111873e55255f150b`  
		Last Modified: Wed, 26 Jan 2022 01:49:55 GMT  
		Size: 25.9 MB (25923216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c695284c12e2e4760a2a37b71f9ed572a621c66646a8fb6336b0dcf6296b13a`  
		Last Modified: Wed, 26 Jan 2022 02:38:51 GMT  
		Size: 49.6 MB (49639076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd03d19014c31feceac42db72787ea78d0fd8a7ffc17bf99ed31807754b1c220`  
		Last Modified: Wed, 26 Jan 2022 02:38:44 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b182d756ce93dcd1597d6ec850f9945f3001407ef3a815a8b209b3b3c573db9`  
		Last Modified: Fri, 04 Feb 2022 22:03:39 GMT  
		Size: 119.7 MB (119699541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.16`

```console
$ docker pull dart@sha256:929127073796cc98376c5cad4633bf2031e4d4f1261dba33b3d65ade4a914d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.16` - linux; amd64

```console
$ docker pull dart@sha256:5615d36ab612eb6edb43f1d6e594c6bf5d4e6f0f83bbb06ddb1ef0822122f69d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280118262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff28224215fa6f9ef187fc0c8a3260a02e1f0f07b834b6502c13c267f27df78`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:35:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:35:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:35:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:35:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:35:56 GMT
WORKDIR /root
# Fri, 04 Feb 2022 21:24:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260f85c7c1aebd4382688a5dd10aa11a241660ea1420867bfa423146bb5e7cb1`  
		Last Modified: Wed, 26 Jan 2022 02:37:06 GMT  
		Size: 49.6 MB (49582700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90aea65c283280db5f2c3e5baf6f94dad74c4970a49c4b080c5ac92da97b09df`  
		Last Modified: Wed, 26 Jan 2022 02:36:55 GMT  
		Size: 2.4 MB (2359153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b3e35b79b51308e44a2c862fcdf7e0f3cfc5f1fc8dfb4bc1865ecc357841d9`  
		Last Modified: Fri, 04 Feb 2022 21:24:57 GMT  
		Size: 201.0 MB (201022678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.16` - linux; arm variant v7

```console
$ docker pull dart@sha256:4dc621f597586d494e3c17cabf16cc81ada7d9fe9cd3a306fec9f37ddf04f13b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186695690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e74cbd7bc9da0eecf553b939f91f6a485476ca81041d0ef37912fe83089cfa1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:43:12 GMT
ADD file:ca8132e20773f7037458cc53fe20a7116f93c21c7479be5a2a1d739495dbe44e in / 
# Wed, 26 Jan 2022 01:43:13 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:25:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:25:00 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:25:01 GMT
WORKDIR /root
# Fri, 04 Feb 2022 21:41:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:20cc49690d9072283406c1c11e9b1dc1a247782cc8daa526b375d4a7f1cb6a94`  
		Last Modified: Wed, 26 Jan 2022 01:59:27 GMT  
		Size: 22.8 MB (22754397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9485b7f36107dac4417e8b7c0659296b3ad4a442719e4b2774a85d71ae3f97`  
		Last Modified: Wed, 26 Jan 2022 02:27:46 GMT  
		Size: 44.4 MB (44399462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19668bef3278d9adb593c7b8625c2956fcf32db075c16ae1fa0af31e948fcc0c`  
		Last Modified: Wed, 26 Jan 2022 02:27:25 GMT  
		Size: 1.4 MB (1355911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2534965437f2a04ef5d3694605b977cbf2ef2a46fe85480e2f7689e08817883d`  
		Last Modified: Fri, 04 Feb 2022 21:44:06 GMT  
		Size: 118.2 MB (118185920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.16` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f0bafd3720e9a797a3740e198ccf9663908253e97d097e44a06661d54ebb751c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196893761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91bb0b5e5082a0bb3112f6ec1dd45fd1aab7220c4a2660569b78fb153828041`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:56 GMT
ADD file:796bc43a948899ba53bddebf7f613769fe96e8ea3a27eb7143d079c7a166ab01 in / 
# Wed, 26 Jan 2022 01:42:57 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:37:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:37:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:37:43 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:37:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:37:45 GMT
WORKDIR /root
# Fri, 04 Feb 2022 22:02:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4c7c9f6f1115fd4f35807a2f6c1375759365a991748aee0111873e55255f150b`  
		Last Modified: Wed, 26 Jan 2022 01:49:55 GMT  
		Size: 25.9 MB (25923216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c695284c12e2e4760a2a37b71f9ed572a621c66646a8fb6336b0dcf6296b13a`  
		Last Modified: Wed, 26 Jan 2022 02:38:51 GMT  
		Size: 49.6 MB (49639076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd03d19014c31feceac42db72787ea78d0fd8a7ffc17bf99ed31807754b1c220`  
		Last Modified: Wed, 26 Jan 2022 02:38:44 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b182d756ce93dcd1597d6ec850f9945f3001407ef3a815a8b209b3b3c573db9`  
		Last Modified: Fri, 04 Feb 2022 22:03:39 GMT  
		Size: 119.7 MB (119699541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.16-sdk`

```console
$ docker pull dart@sha256:929127073796cc98376c5cad4633bf2031e4d4f1261dba33b3d65ade4a914d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.16-sdk` - linux; amd64

```console
$ docker pull dart@sha256:5615d36ab612eb6edb43f1d6e594c6bf5d4e6f0f83bbb06ddb1ef0822122f69d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280118262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff28224215fa6f9ef187fc0c8a3260a02e1f0f07b834b6502c13c267f27df78`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:35:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:35:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:35:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:35:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:35:56 GMT
WORKDIR /root
# Fri, 04 Feb 2022 21:24:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260f85c7c1aebd4382688a5dd10aa11a241660ea1420867bfa423146bb5e7cb1`  
		Last Modified: Wed, 26 Jan 2022 02:37:06 GMT  
		Size: 49.6 MB (49582700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90aea65c283280db5f2c3e5baf6f94dad74c4970a49c4b080c5ac92da97b09df`  
		Last Modified: Wed, 26 Jan 2022 02:36:55 GMT  
		Size: 2.4 MB (2359153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b3e35b79b51308e44a2c862fcdf7e0f3cfc5f1fc8dfb4bc1865ecc357841d9`  
		Last Modified: Fri, 04 Feb 2022 21:24:57 GMT  
		Size: 201.0 MB (201022678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.16-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:4dc621f597586d494e3c17cabf16cc81ada7d9fe9cd3a306fec9f37ddf04f13b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186695690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e74cbd7bc9da0eecf553b939f91f6a485476ca81041d0ef37912fe83089cfa1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:43:12 GMT
ADD file:ca8132e20773f7037458cc53fe20a7116f93c21c7479be5a2a1d739495dbe44e in / 
# Wed, 26 Jan 2022 01:43:13 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:25:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:25:00 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:25:01 GMT
WORKDIR /root
# Fri, 04 Feb 2022 21:41:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:20cc49690d9072283406c1c11e9b1dc1a247782cc8daa526b375d4a7f1cb6a94`  
		Last Modified: Wed, 26 Jan 2022 01:59:27 GMT  
		Size: 22.8 MB (22754397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9485b7f36107dac4417e8b7c0659296b3ad4a442719e4b2774a85d71ae3f97`  
		Last Modified: Wed, 26 Jan 2022 02:27:46 GMT  
		Size: 44.4 MB (44399462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19668bef3278d9adb593c7b8625c2956fcf32db075c16ae1fa0af31e948fcc0c`  
		Last Modified: Wed, 26 Jan 2022 02:27:25 GMT  
		Size: 1.4 MB (1355911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2534965437f2a04ef5d3694605b977cbf2ef2a46fe85480e2f7689e08817883d`  
		Last Modified: Fri, 04 Feb 2022 21:44:06 GMT  
		Size: 118.2 MB (118185920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.16-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f0bafd3720e9a797a3740e198ccf9663908253e97d097e44a06661d54ebb751c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196893761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91bb0b5e5082a0bb3112f6ec1dd45fd1aab7220c4a2660569b78fb153828041`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:56 GMT
ADD file:796bc43a948899ba53bddebf7f613769fe96e8ea3a27eb7143d079c7a166ab01 in / 
# Wed, 26 Jan 2022 01:42:57 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:37:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:37:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:37:43 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:37:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:37:45 GMT
WORKDIR /root
# Fri, 04 Feb 2022 22:02:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4c7c9f6f1115fd4f35807a2f6c1375759365a991748aee0111873e55255f150b`  
		Last Modified: Wed, 26 Jan 2022 01:49:55 GMT  
		Size: 25.9 MB (25923216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c695284c12e2e4760a2a37b71f9ed572a621c66646a8fb6336b0dcf6296b13a`  
		Last Modified: Wed, 26 Jan 2022 02:38:51 GMT  
		Size: 49.6 MB (49639076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd03d19014c31feceac42db72787ea78d0fd8a7ffc17bf99ed31807754b1c220`  
		Last Modified: Wed, 26 Jan 2022 02:38:44 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b182d756ce93dcd1597d6ec850f9945f3001407ef3a815a8b209b3b3c573db9`  
		Last Modified: Fri, 04 Feb 2022 22:03:39 GMT  
		Size: 119.7 MB (119699541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.16.0`

```console
$ docker pull dart@sha256:929127073796cc98376c5cad4633bf2031e4d4f1261dba33b3d65ade4a914d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.16.0` - linux; amd64

```console
$ docker pull dart@sha256:5615d36ab612eb6edb43f1d6e594c6bf5d4e6f0f83bbb06ddb1ef0822122f69d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280118262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff28224215fa6f9ef187fc0c8a3260a02e1f0f07b834b6502c13c267f27df78`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:35:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:35:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:35:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:35:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:35:56 GMT
WORKDIR /root
# Fri, 04 Feb 2022 21:24:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260f85c7c1aebd4382688a5dd10aa11a241660ea1420867bfa423146bb5e7cb1`  
		Last Modified: Wed, 26 Jan 2022 02:37:06 GMT  
		Size: 49.6 MB (49582700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90aea65c283280db5f2c3e5baf6f94dad74c4970a49c4b080c5ac92da97b09df`  
		Last Modified: Wed, 26 Jan 2022 02:36:55 GMT  
		Size: 2.4 MB (2359153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b3e35b79b51308e44a2c862fcdf7e0f3cfc5f1fc8dfb4bc1865ecc357841d9`  
		Last Modified: Fri, 04 Feb 2022 21:24:57 GMT  
		Size: 201.0 MB (201022678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.16.0` - linux; arm variant v7

```console
$ docker pull dart@sha256:4dc621f597586d494e3c17cabf16cc81ada7d9fe9cd3a306fec9f37ddf04f13b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186695690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e74cbd7bc9da0eecf553b939f91f6a485476ca81041d0ef37912fe83089cfa1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:43:12 GMT
ADD file:ca8132e20773f7037458cc53fe20a7116f93c21c7479be5a2a1d739495dbe44e in / 
# Wed, 26 Jan 2022 01:43:13 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:25:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:25:00 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:25:01 GMT
WORKDIR /root
# Fri, 04 Feb 2022 21:41:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:20cc49690d9072283406c1c11e9b1dc1a247782cc8daa526b375d4a7f1cb6a94`  
		Last Modified: Wed, 26 Jan 2022 01:59:27 GMT  
		Size: 22.8 MB (22754397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9485b7f36107dac4417e8b7c0659296b3ad4a442719e4b2774a85d71ae3f97`  
		Last Modified: Wed, 26 Jan 2022 02:27:46 GMT  
		Size: 44.4 MB (44399462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19668bef3278d9adb593c7b8625c2956fcf32db075c16ae1fa0af31e948fcc0c`  
		Last Modified: Wed, 26 Jan 2022 02:27:25 GMT  
		Size: 1.4 MB (1355911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2534965437f2a04ef5d3694605b977cbf2ef2a46fe85480e2f7689e08817883d`  
		Last Modified: Fri, 04 Feb 2022 21:44:06 GMT  
		Size: 118.2 MB (118185920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.16.0` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f0bafd3720e9a797a3740e198ccf9663908253e97d097e44a06661d54ebb751c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196893761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91bb0b5e5082a0bb3112f6ec1dd45fd1aab7220c4a2660569b78fb153828041`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:56 GMT
ADD file:796bc43a948899ba53bddebf7f613769fe96e8ea3a27eb7143d079c7a166ab01 in / 
# Wed, 26 Jan 2022 01:42:57 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:37:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:37:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:37:43 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:37:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:37:45 GMT
WORKDIR /root
# Fri, 04 Feb 2022 22:02:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4c7c9f6f1115fd4f35807a2f6c1375759365a991748aee0111873e55255f150b`  
		Last Modified: Wed, 26 Jan 2022 01:49:55 GMT  
		Size: 25.9 MB (25923216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c695284c12e2e4760a2a37b71f9ed572a621c66646a8fb6336b0dcf6296b13a`  
		Last Modified: Wed, 26 Jan 2022 02:38:51 GMT  
		Size: 49.6 MB (49639076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd03d19014c31feceac42db72787ea78d0fd8a7ffc17bf99ed31807754b1c220`  
		Last Modified: Wed, 26 Jan 2022 02:38:44 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b182d756ce93dcd1597d6ec850f9945f3001407ef3a815a8b209b3b3c573db9`  
		Last Modified: Fri, 04 Feb 2022 22:03:39 GMT  
		Size: 119.7 MB (119699541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.16.0-sdk`

```console
$ docker pull dart@sha256:929127073796cc98376c5cad4633bf2031e4d4f1261dba33b3d65ade4a914d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.16.0-sdk` - linux; amd64

```console
$ docker pull dart@sha256:5615d36ab612eb6edb43f1d6e594c6bf5d4e6f0f83bbb06ddb1ef0822122f69d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280118262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff28224215fa6f9ef187fc0c8a3260a02e1f0f07b834b6502c13c267f27df78`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:35:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:35:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:35:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:35:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:35:56 GMT
WORKDIR /root
# Fri, 04 Feb 2022 21:24:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260f85c7c1aebd4382688a5dd10aa11a241660ea1420867bfa423146bb5e7cb1`  
		Last Modified: Wed, 26 Jan 2022 02:37:06 GMT  
		Size: 49.6 MB (49582700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90aea65c283280db5f2c3e5baf6f94dad74c4970a49c4b080c5ac92da97b09df`  
		Last Modified: Wed, 26 Jan 2022 02:36:55 GMT  
		Size: 2.4 MB (2359153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b3e35b79b51308e44a2c862fcdf7e0f3cfc5f1fc8dfb4bc1865ecc357841d9`  
		Last Modified: Fri, 04 Feb 2022 21:24:57 GMT  
		Size: 201.0 MB (201022678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.16.0-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:4dc621f597586d494e3c17cabf16cc81ada7d9fe9cd3a306fec9f37ddf04f13b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186695690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e74cbd7bc9da0eecf553b939f91f6a485476ca81041d0ef37912fe83089cfa1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:43:12 GMT
ADD file:ca8132e20773f7037458cc53fe20a7116f93c21c7479be5a2a1d739495dbe44e in / 
# Wed, 26 Jan 2022 01:43:13 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:25:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:25:00 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:25:01 GMT
WORKDIR /root
# Fri, 04 Feb 2022 21:41:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:20cc49690d9072283406c1c11e9b1dc1a247782cc8daa526b375d4a7f1cb6a94`  
		Last Modified: Wed, 26 Jan 2022 01:59:27 GMT  
		Size: 22.8 MB (22754397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9485b7f36107dac4417e8b7c0659296b3ad4a442719e4b2774a85d71ae3f97`  
		Last Modified: Wed, 26 Jan 2022 02:27:46 GMT  
		Size: 44.4 MB (44399462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19668bef3278d9adb593c7b8625c2956fcf32db075c16ae1fa0af31e948fcc0c`  
		Last Modified: Wed, 26 Jan 2022 02:27:25 GMT  
		Size: 1.4 MB (1355911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2534965437f2a04ef5d3694605b977cbf2ef2a46fe85480e2f7689e08817883d`  
		Last Modified: Fri, 04 Feb 2022 21:44:06 GMT  
		Size: 118.2 MB (118185920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.16.0-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f0bafd3720e9a797a3740e198ccf9663908253e97d097e44a06661d54ebb751c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196893761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91bb0b5e5082a0bb3112f6ec1dd45fd1aab7220c4a2660569b78fb153828041`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:56 GMT
ADD file:796bc43a948899ba53bddebf7f613769fe96e8ea3a27eb7143d079c7a166ab01 in / 
# Wed, 26 Jan 2022 01:42:57 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:37:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:37:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:37:43 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:37:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:37:45 GMT
WORKDIR /root
# Fri, 04 Feb 2022 22:02:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4c7c9f6f1115fd4f35807a2f6c1375759365a991748aee0111873e55255f150b`  
		Last Modified: Wed, 26 Jan 2022 01:49:55 GMT  
		Size: 25.9 MB (25923216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c695284c12e2e4760a2a37b71f9ed572a621c66646a8fb6336b0dcf6296b13a`  
		Last Modified: Wed, 26 Jan 2022 02:38:51 GMT  
		Size: 49.6 MB (49639076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd03d19014c31feceac42db72787ea78d0fd8a7ffc17bf99ed31807754b1c220`  
		Last Modified: Wed, 26 Jan 2022 02:38:44 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b182d756ce93dcd1597d6ec850f9945f3001407ef3a815a8b209b3b3c573db9`  
		Last Modified: Fri, 04 Feb 2022 22:03:39 GMT  
		Size: 119.7 MB (119699541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta`

```console
$ docker pull dart@sha256:929127073796cc98376c5cad4633bf2031e4d4f1261dba33b3d65ade4a914d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:5615d36ab612eb6edb43f1d6e594c6bf5d4e6f0f83bbb06ddb1ef0822122f69d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280118262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff28224215fa6f9ef187fc0c8a3260a02e1f0f07b834b6502c13c267f27df78`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:35:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:35:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:35:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:35:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:35:56 GMT
WORKDIR /root
# Fri, 04 Feb 2022 21:24:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260f85c7c1aebd4382688a5dd10aa11a241660ea1420867bfa423146bb5e7cb1`  
		Last Modified: Wed, 26 Jan 2022 02:37:06 GMT  
		Size: 49.6 MB (49582700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90aea65c283280db5f2c3e5baf6f94dad74c4970a49c4b080c5ac92da97b09df`  
		Last Modified: Wed, 26 Jan 2022 02:36:55 GMT  
		Size: 2.4 MB (2359153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b3e35b79b51308e44a2c862fcdf7e0f3cfc5f1fc8dfb4bc1865ecc357841d9`  
		Last Modified: Fri, 04 Feb 2022 21:24:57 GMT  
		Size: 201.0 MB (201022678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:4dc621f597586d494e3c17cabf16cc81ada7d9fe9cd3a306fec9f37ddf04f13b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186695690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e74cbd7bc9da0eecf553b939f91f6a485476ca81041d0ef37912fe83089cfa1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:43:12 GMT
ADD file:ca8132e20773f7037458cc53fe20a7116f93c21c7479be5a2a1d739495dbe44e in / 
# Wed, 26 Jan 2022 01:43:13 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:25:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:25:00 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:25:01 GMT
WORKDIR /root
# Fri, 04 Feb 2022 21:41:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:20cc49690d9072283406c1c11e9b1dc1a247782cc8daa526b375d4a7f1cb6a94`  
		Last Modified: Wed, 26 Jan 2022 01:59:27 GMT  
		Size: 22.8 MB (22754397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9485b7f36107dac4417e8b7c0659296b3ad4a442719e4b2774a85d71ae3f97`  
		Last Modified: Wed, 26 Jan 2022 02:27:46 GMT  
		Size: 44.4 MB (44399462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19668bef3278d9adb593c7b8625c2956fcf32db075c16ae1fa0af31e948fcc0c`  
		Last Modified: Wed, 26 Jan 2022 02:27:25 GMT  
		Size: 1.4 MB (1355911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2534965437f2a04ef5d3694605b977cbf2ef2a46fe85480e2f7689e08817883d`  
		Last Modified: Fri, 04 Feb 2022 21:44:06 GMT  
		Size: 118.2 MB (118185920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f0bafd3720e9a797a3740e198ccf9663908253e97d097e44a06661d54ebb751c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196893761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91bb0b5e5082a0bb3112f6ec1dd45fd1aab7220c4a2660569b78fb153828041`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:56 GMT
ADD file:796bc43a948899ba53bddebf7f613769fe96e8ea3a27eb7143d079c7a166ab01 in / 
# Wed, 26 Jan 2022 01:42:57 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:37:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:37:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:37:43 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:37:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:37:45 GMT
WORKDIR /root
# Fri, 04 Feb 2022 22:02:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4c7c9f6f1115fd4f35807a2f6c1375759365a991748aee0111873e55255f150b`  
		Last Modified: Wed, 26 Jan 2022 01:49:55 GMT  
		Size: 25.9 MB (25923216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c695284c12e2e4760a2a37b71f9ed572a621c66646a8fb6336b0dcf6296b13a`  
		Last Modified: Wed, 26 Jan 2022 02:38:51 GMT  
		Size: 49.6 MB (49639076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd03d19014c31feceac42db72787ea78d0fd8a7ffc17bf99ed31807754b1c220`  
		Last Modified: Wed, 26 Jan 2022 02:38:44 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b182d756ce93dcd1597d6ec850f9945f3001407ef3a815a8b209b3b3c573db9`  
		Last Modified: Fri, 04 Feb 2022 22:03:39 GMT  
		Size: 119.7 MB (119699541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:929127073796cc98376c5cad4633bf2031e4d4f1261dba33b3d65ade4a914d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:5615d36ab612eb6edb43f1d6e594c6bf5d4e6f0f83bbb06ddb1ef0822122f69d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280118262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff28224215fa6f9ef187fc0c8a3260a02e1f0f07b834b6502c13c267f27df78`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:35:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:35:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:35:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:35:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:35:56 GMT
WORKDIR /root
# Fri, 04 Feb 2022 21:24:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260f85c7c1aebd4382688a5dd10aa11a241660ea1420867bfa423146bb5e7cb1`  
		Last Modified: Wed, 26 Jan 2022 02:37:06 GMT  
		Size: 49.6 MB (49582700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90aea65c283280db5f2c3e5baf6f94dad74c4970a49c4b080c5ac92da97b09df`  
		Last Modified: Wed, 26 Jan 2022 02:36:55 GMT  
		Size: 2.4 MB (2359153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b3e35b79b51308e44a2c862fcdf7e0f3cfc5f1fc8dfb4bc1865ecc357841d9`  
		Last Modified: Fri, 04 Feb 2022 21:24:57 GMT  
		Size: 201.0 MB (201022678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:4dc621f597586d494e3c17cabf16cc81ada7d9fe9cd3a306fec9f37ddf04f13b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186695690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e74cbd7bc9da0eecf553b939f91f6a485476ca81041d0ef37912fe83089cfa1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:43:12 GMT
ADD file:ca8132e20773f7037458cc53fe20a7116f93c21c7479be5a2a1d739495dbe44e in / 
# Wed, 26 Jan 2022 01:43:13 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:25:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:25:00 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:25:01 GMT
WORKDIR /root
# Fri, 04 Feb 2022 21:41:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:20cc49690d9072283406c1c11e9b1dc1a247782cc8daa526b375d4a7f1cb6a94`  
		Last Modified: Wed, 26 Jan 2022 01:59:27 GMT  
		Size: 22.8 MB (22754397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9485b7f36107dac4417e8b7c0659296b3ad4a442719e4b2774a85d71ae3f97`  
		Last Modified: Wed, 26 Jan 2022 02:27:46 GMT  
		Size: 44.4 MB (44399462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19668bef3278d9adb593c7b8625c2956fcf32db075c16ae1fa0af31e948fcc0c`  
		Last Modified: Wed, 26 Jan 2022 02:27:25 GMT  
		Size: 1.4 MB (1355911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2534965437f2a04ef5d3694605b977cbf2ef2a46fe85480e2f7689e08817883d`  
		Last Modified: Fri, 04 Feb 2022 21:44:06 GMT  
		Size: 118.2 MB (118185920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f0bafd3720e9a797a3740e198ccf9663908253e97d097e44a06661d54ebb751c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196893761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91bb0b5e5082a0bb3112f6ec1dd45fd1aab7220c4a2660569b78fb153828041`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:56 GMT
ADD file:796bc43a948899ba53bddebf7f613769fe96e8ea3a27eb7143d079c7a166ab01 in / 
# Wed, 26 Jan 2022 01:42:57 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:37:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:37:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:37:43 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:37:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:37:45 GMT
WORKDIR /root
# Fri, 04 Feb 2022 22:02:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4c7c9f6f1115fd4f35807a2f6c1375759365a991748aee0111873e55255f150b`  
		Last Modified: Wed, 26 Jan 2022 01:49:55 GMT  
		Size: 25.9 MB (25923216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c695284c12e2e4760a2a37b71f9ed572a621c66646a8fb6336b0dcf6296b13a`  
		Last Modified: Wed, 26 Jan 2022 02:38:51 GMT  
		Size: 49.6 MB (49639076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd03d19014c31feceac42db72787ea78d0fd8a7ffc17bf99ed31807754b1c220`  
		Last Modified: Wed, 26 Jan 2022 02:38:44 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b182d756ce93dcd1597d6ec850f9945f3001407ef3a815a8b209b3b3c573db9`  
		Last Modified: Fri, 04 Feb 2022 22:03:39 GMT  
		Size: 119.7 MB (119699541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:latest`

```console
$ docker pull dart@sha256:929127073796cc98376c5cad4633bf2031e4d4f1261dba33b3d65ade4a914d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:5615d36ab612eb6edb43f1d6e594c6bf5d4e6f0f83bbb06ddb1ef0822122f69d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280118262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff28224215fa6f9ef187fc0c8a3260a02e1f0f07b834b6502c13c267f27df78`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:35:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:35:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:35:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:35:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:35:56 GMT
WORKDIR /root
# Fri, 04 Feb 2022 21:24:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260f85c7c1aebd4382688a5dd10aa11a241660ea1420867bfa423146bb5e7cb1`  
		Last Modified: Wed, 26 Jan 2022 02:37:06 GMT  
		Size: 49.6 MB (49582700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90aea65c283280db5f2c3e5baf6f94dad74c4970a49c4b080c5ac92da97b09df`  
		Last Modified: Wed, 26 Jan 2022 02:36:55 GMT  
		Size: 2.4 MB (2359153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b3e35b79b51308e44a2c862fcdf7e0f3cfc5f1fc8dfb4bc1865ecc357841d9`  
		Last Modified: Fri, 04 Feb 2022 21:24:57 GMT  
		Size: 201.0 MB (201022678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:4dc621f597586d494e3c17cabf16cc81ada7d9fe9cd3a306fec9f37ddf04f13b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186695690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e74cbd7bc9da0eecf553b939f91f6a485476ca81041d0ef37912fe83089cfa1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:43:12 GMT
ADD file:ca8132e20773f7037458cc53fe20a7116f93c21c7479be5a2a1d739495dbe44e in / 
# Wed, 26 Jan 2022 01:43:13 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:25:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:25:00 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:25:01 GMT
WORKDIR /root
# Fri, 04 Feb 2022 21:41:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:20cc49690d9072283406c1c11e9b1dc1a247782cc8daa526b375d4a7f1cb6a94`  
		Last Modified: Wed, 26 Jan 2022 01:59:27 GMT  
		Size: 22.8 MB (22754397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9485b7f36107dac4417e8b7c0659296b3ad4a442719e4b2774a85d71ae3f97`  
		Last Modified: Wed, 26 Jan 2022 02:27:46 GMT  
		Size: 44.4 MB (44399462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19668bef3278d9adb593c7b8625c2956fcf32db075c16ae1fa0af31e948fcc0c`  
		Last Modified: Wed, 26 Jan 2022 02:27:25 GMT  
		Size: 1.4 MB (1355911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2534965437f2a04ef5d3694605b977cbf2ef2a46fe85480e2f7689e08817883d`  
		Last Modified: Fri, 04 Feb 2022 21:44:06 GMT  
		Size: 118.2 MB (118185920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f0bafd3720e9a797a3740e198ccf9663908253e97d097e44a06661d54ebb751c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196893761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91bb0b5e5082a0bb3112f6ec1dd45fd1aab7220c4a2660569b78fb153828041`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:56 GMT
ADD file:796bc43a948899ba53bddebf7f613769fe96e8ea3a27eb7143d079c7a166ab01 in / 
# Wed, 26 Jan 2022 01:42:57 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:37:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:37:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:37:43 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:37:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:37:45 GMT
WORKDIR /root
# Fri, 04 Feb 2022 22:02:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4c7c9f6f1115fd4f35807a2f6c1375759365a991748aee0111873e55255f150b`  
		Last Modified: Wed, 26 Jan 2022 01:49:55 GMT  
		Size: 25.9 MB (25923216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c695284c12e2e4760a2a37b71f9ed572a621c66646a8fb6336b0dcf6296b13a`  
		Last Modified: Wed, 26 Jan 2022 02:38:51 GMT  
		Size: 49.6 MB (49639076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd03d19014c31feceac42db72787ea78d0fd8a7ffc17bf99ed31807754b1c220`  
		Last Modified: Wed, 26 Jan 2022 02:38:44 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b182d756ce93dcd1597d6ec850f9945f3001407ef3a815a8b209b3b3c573db9`  
		Last Modified: Fri, 04 Feb 2022 22:03:39 GMT  
		Size: 119.7 MB (119699541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:sdk`

```console
$ docker pull dart@sha256:929127073796cc98376c5cad4633bf2031e4d4f1261dba33b3d65ade4a914d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:5615d36ab612eb6edb43f1d6e594c6bf5d4e6f0f83bbb06ddb1ef0822122f69d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280118262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff28224215fa6f9ef187fc0c8a3260a02e1f0f07b834b6502c13c267f27df78`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:35:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:35:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:35:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:35:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:35:56 GMT
WORKDIR /root
# Fri, 04 Feb 2022 21:24:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260f85c7c1aebd4382688a5dd10aa11a241660ea1420867bfa423146bb5e7cb1`  
		Last Modified: Wed, 26 Jan 2022 02:37:06 GMT  
		Size: 49.6 MB (49582700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90aea65c283280db5f2c3e5baf6f94dad74c4970a49c4b080c5ac92da97b09df`  
		Last Modified: Wed, 26 Jan 2022 02:36:55 GMT  
		Size: 2.4 MB (2359153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b3e35b79b51308e44a2c862fcdf7e0f3cfc5f1fc8dfb4bc1865ecc357841d9`  
		Last Modified: Fri, 04 Feb 2022 21:24:57 GMT  
		Size: 201.0 MB (201022678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:4dc621f597586d494e3c17cabf16cc81ada7d9fe9cd3a306fec9f37ddf04f13b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186695690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e74cbd7bc9da0eecf553b939f91f6a485476ca81041d0ef37912fe83089cfa1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:43:12 GMT
ADD file:ca8132e20773f7037458cc53fe20a7116f93c21c7479be5a2a1d739495dbe44e in / 
# Wed, 26 Jan 2022 01:43:13 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:25:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:25:00 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:25:01 GMT
WORKDIR /root
# Fri, 04 Feb 2022 21:41:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:20cc49690d9072283406c1c11e9b1dc1a247782cc8daa526b375d4a7f1cb6a94`  
		Last Modified: Wed, 26 Jan 2022 01:59:27 GMT  
		Size: 22.8 MB (22754397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9485b7f36107dac4417e8b7c0659296b3ad4a442719e4b2774a85d71ae3f97`  
		Last Modified: Wed, 26 Jan 2022 02:27:46 GMT  
		Size: 44.4 MB (44399462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19668bef3278d9adb593c7b8625c2956fcf32db075c16ae1fa0af31e948fcc0c`  
		Last Modified: Wed, 26 Jan 2022 02:27:25 GMT  
		Size: 1.4 MB (1355911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2534965437f2a04ef5d3694605b977cbf2ef2a46fe85480e2f7689e08817883d`  
		Last Modified: Fri, 04 Feb 2022 21:44:06 GMT  
		Size: 118.2 MB (118185920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f0bafd3720e9a797a3740e198ccf9663908253e97d097e44a06661d54ebb751c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196893761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91bb0b5e5082a0bb3112f6ec1dd45fd1aab7220c4a2660569b78fb153828041`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:56 GMT
ADD file:796bc43a948899ba53bddebf7f613769fe96e8ea3a27eb7143d079c7a166ab01 in / 
# Wed, 26 Jan 2022 01:42:57 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:37:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:37:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:37:43 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:37:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:37:45 GMT
WORKDIR /root
# Fri, 04 Feb 2022 22:02:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4c7c9f6f1115fd4f35807a2f6c1375759365a991748aee0111873e55255f150b`  
		Last Modified: Wed, 26 Jan 2022 01:49:55 GMT  
		Size: 25.9 MB (25923216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c695284c12e2e4760a2a37b71f9ed572a621c66646a8fb6336b0dcf6296b13a`  
		Last Modified: Wed, 26 Jan 2022 02:38:51 GMT  
		Size: 49.6 MB (49639076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd03d19014c31feceac42db72787ea78d0fd8a7ffc17bf99ed31807754b1c220`  
		Last Modified: Wed, 26 Jan 2022 02:38:44 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b182d756ce93dcd1597d6ec850f9945f3001407ef3a815a8b209b3b3c573db9`  
		Last Modified: Fri, 04 Feb 2022 22:03:39 GMT  
		Size: 119.7 MB (119699541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable`

```console
$ docker pull dart@sha256:929127073796cc98376c5cad4633bf2031e4d4f1261dba33b3d65ade4a914d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:5615d36ab612eb6edb43f1d6e594c6bf5d4e6f0f83bbb06ddb1ef0822122f69d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280118262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff28224215fa6f9ef187fc0c8a3260a02e1f0f07b834b6502c13c267f27df78`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:35:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:35:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:35:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:35:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:35:56 GMT
WORKDIR /root
# Fri, 04 Feb 2022 21:24:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260f85c7c1aebd4382688a5dd10aa11a241660ea1420867bfa423146bb5e7cb1`  
		Last Modified: Wed, 26 Jan 2022 02:37:06 GMT  
		Size: 49.6 MB (49582700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90aea65c283280db5f2c3e5baf6f94dad74c4970a49c4b080c5ac92da97b09df`  
		Last Modified: Wed, 26 Jan 2022 02:36:55 GMT  
		Size: 2.4 MB (2359153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b3e35b79b51308e44a2c862fcdf7e0f3cfc5f1fc8dfb4bc1865ecc357841d9`  
		Last Modified: Fri, 04 Feb 2022 21:24:57 GMT  
		Size: 201.0 MB (201022678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:4dc621f597586d494e3c17cabf16cc81ada7d9fe9cd3a306fec9f37ddf04f13b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186695690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e74cbd7bc9da0eecf553b939f91f6a485476ca81041d0ef37912fe83089cfa1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:43:12 GMT
ADD file:ca8132e20773f7037458cc53fe20a7116f93c21c7479be5a2a1d739495dbe44e in / 
# Wed, 26 Jan 2022 01:43:13 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:25:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:25:00 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:25:01 GMT
WORKDIR /root
# Fri, 04 Feb 2022 21:41:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:20cc49690d9072283406c1c11e9b1dc1a247782cc8daa526b375d4a7f1cb6a94`  
		Last Modified: Wed, 26 Jan 2022 01:59:27 GMT  
		Size: 22.8 MB (22754397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9485b7f36107dac4417e8b7c0659296b3ad4a442719e4b2774a85d71ae3f97`  
		Last Modified: Wed, 26 Jan 2022 02:27:46 GMT  
		Size: 44.4 MB (44399462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19668bef3278d9adb593c7b8625c2956fcf32db075c16ae1fa0af31e948fcc0c`  
		Last Modified: Wed, 26 Jan 2022 02:27:25 GMT  
		Size: 1.4 MB (1355911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2534965437f2a04ef5d3694605b977cbf2ef2a46fe85480e2f7689e08817883d`  
		Last Modified: Fri, 04 Feb 2022 21:44:06 GMT  
		Size: 118.2 MB (118185920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f0bafd3720e9a797a3740e198ccf9663908253e97d097e44a06661d54ebb751c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196893761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91bb0b5e5082a0bb3112f6ec1dd45fd1aab7220c4a2660569b78fb153828041`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:56 GMT
ADD file:796bc43a948899ba53bddebf7f613769fe96e8ea3a27eb7143d079c7a166ab01 in / 
# Wed, 26 Jan 2022 01:42:57 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:37:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:37:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:37:43 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:37:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:37:45 GMT
WORKDIR /root
# Fri, 04 Feb 2022 22:02:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4c7c9f6f1115fd4f35807a2f6c1375759365a991748aee0111873e55255f150b`  
		Last Modified: Wed, 26 Jan 2022 01:49:55 GMT  
		Size: 25.9 MB (25923216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c695284c12e2e4760a2a37b71f9ed572a621c66646a8fb6336b0dcf6296b13a`  
		Last Modified: Wed, 26 Jan 2022 02:38:51 GMT  
		Size: 49.6 MB (49639076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd03d19014c31feceac42db72787ea78d0fd8a7ffc17bf99ed31807754b1c220`  
		Last Modified: Wed, 26 Jan 2022 02:38:44 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b182d756ce93dcd1597d6ec850f9945f3001407ef3a815a8b209b3b3c573db9`  
		Last Modified: Fri, 04 Feb 2022 22:03:39 GMT  
		Size: 119.7 MB (119699541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:929127073796cc98376c5cad4633bf2031e4d4f1261dba33b3d65ade4a914d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:5615d36ab612eb6edb43f1d6e594c6bf5d4e6f0f83bbb06ddb1ef0822122f69d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280118262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff28224215fa6f9ef187fc0c8a3260a02e1f0f07b834b6502c13c267f27df78`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:35:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:35:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:35:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:35:56 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:35:56 GMT
WORKDIR /root
# Fri, 04 Feb 2022 21:24:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260f85c7c1aebd4382688a5dd10aa11a241660ea1420867bfa423146bb5e7cb1`  
		Last Modified: Wed, 26 Jan 2022 02:37:06 GMT  
		Size: 49.6 MB (49582700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90aea65c283280db5f2c3e5baf6f94dad74c4970a49c4b080c5ac92da97b09df`  
		Last Modified: Wed, 26 Jan 2022 02:36:55 GMT  
		Size: 2.4 MB (2359153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b3e35b79b51308e44a2c862fcdf7e0f3cfc5f1fc8dfb4bc1865ecc357841d9`  
		Last Modified: Fri, 04 Feb 2022 21:24:57 GMT  
		Size: 201.0 MB (201022678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:4dc621f597586d494e3c17cabf16cc81ada7d9fe9cd3a306fec9f37ddf04f13b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186695690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e74cbd7bc9da0eecf553b939f91f6a485476ca81041d0ef37912fe83089cfa1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:43:12 GMT
ADD file:ca8132e20773f7037458cc53fe20a7116f93c21c7479be5a2a1d739495dbe44e in / 
# Wed, 26 Jan 2022 01:43:13 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:24:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:25:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:25:00 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:25:01 GMT
WORKDIR /root
# Fri, 04 Feb 2022 21:41:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:20cc49690d9072283406c1c11e9b1dc1a247782cc8daa526b375d4a7f1cb6a94`  
		Last Modified: Wed, 26 Jan 2022 01:59:27 GMT  
		Size: 22.8 MB (22754397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9485b7f36107dac4417e8b7c0659296b3ad4a442719e4b2774a85d71ae3f97`  
		Last Modified: Wed, 26 Jan 2022 02:27:46 GMT  
		Size: 44.4 MB (44399462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19668bef3278d9adb593c7b8625c2956fcf32db075c16ae1fa0af31e948fcc0c`  
		Last Modified: Wed, 26 Jan 2022 02:27:25 GMT  
		Size: 1.4 MB (1355911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2534965437f2a04ef5d3694605b977cbf2ef2a46fe85480e2f7689e08817883d`  
		Last Modified: Fri, 04 Feb 2022 21:44:06 GMT  
		Size: 118.2 MB (118185920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f0bafd3720e9a797a3740e198ccf9663908253e97d097e44a06661d54ebb751c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196893761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91bb0b5e5082a0bb3112f6ec1dd45fd1aab7220c4a2660569b78fb153828041`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:56 GMT
ADD file:796bc43a948899ba53bddebf7f613769fe96e8ea3a27eb7143d079c7a166ab01 in / 
# Wed, 26 Jan 2022 01:42:57 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:37:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:37:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 26 Jan 2022 02:37:43 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 26 Jan 2022 02:37:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 02:37:45 GMT
WORKDIR /root
# Fri, 04 Feb 2022 22:02:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9fe86bde232de52d2211e47f5fdcc143ce936e309a8da1b447213e223d7f68d3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b2420751b9661f2d8c89931fdffdc915526889291b345911c310487d3274f56b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=34e08cd8412a7a40265d202630a2220df82589d353d106dc3bc4a902fd44060b;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4c7c9f6f1115fd4f35807a2f6c1375759365a991748aee0111873e55255f150b`  
		Last Modified: Wed, 26 Jan 2022 01:49:55 GMT  
		Size: 25.9 MB (25923216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c695284c12e2e4760a2a37b71f9ed572a621c66646a8fb6336b0dcf6296b13a`  
		Last Modified: Wed, 26 Jan 2022 02:38:51 GMT  
		Size: 49.6 MB (49639076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd03d19014c31feceac42db72787ea78d0fd8a7ffc17bf99ed31807754b1c220`  
		Last Modified: Wed, 26 Jan 2022 02:38:44 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b182d756ce93dcd1597d6ec850f9945f3001407ef3a815a8b209b3b3c573db9`  
		Last Modified: Fri, 04 Feb 2022 22:03:39 GMT  
		Size: 119.7 MB (119699541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
