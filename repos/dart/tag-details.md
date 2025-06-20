<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.8`](#dart38)
-	[`dart:3.8-sdk`](#dart38-sdk)
-	[`dart:3.8.1`](#dart381)
-	[`dart:3.8.1-sdk`](#dart381-sdk)
-	[`dart:3.9.0-196.1.beta`](#dart390-1961beta)
-	[`dart:3.9.0-196.1.beta-sdk`](#dart390-1961beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:50056357ebfe43304527d5c811f537be8e2675f3460b719c6083eb89d2791517
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3` - linux; amd64

```console
$ docker pull dart@sha256:957afa52747de2fd6222741c0eb3abb06d3aee7b4b042c30eb8fdce32ac69af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285790189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4f3493981e07d7cb55687a8ba0c992f71bab9172c5b4fe555a93709907ad1f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309573cdb83d25db63305504108d32d9c8e4b326521651232684ce334b9ed75d`  
		Last Modified: Tue, 10 Jun 2025 23:37:56 GMT  
		Size: 54.9 MB (54910529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f693390485d0102e4afcc6882973e00e0737029d9b78684e19ab97d7041b3761`  
		Last Modified: Tue, 10 Jun 2025 23:37:53 GMT  
		Size: 1.8 MB (1785451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278953d6a98dbb5b3ae9f0b38fd5faaab6c6cfaa44021397bab7be1281e2d2fb`  
		Last Modified: Wed, 11 Jun 2025 02:53:51 GMT  
		Size: 200.9 MB (200864048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:c355799bf4df5cbc2a36ede6a8be2ae9f88b075dcd7eda7eea100fab50febe7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e6bd61dc498fc8e05c902861afb82f2341f7e2482177dae54b01e61fb0a34e`

```dockerfile
```

-	Layers:
	-	`sha256:be3f7a30f8d54b4c070d59c6aaa5b4c18594593c7e38c4ecde8a98b63e0a8450`  
		Last Modified: Wed, 11 Jun 2025 02:53:18 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:0d6c4e08a0df4341ab8754418d43a6df4ebc2059579b9e8ddfb040402f5934b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214490678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9f47c2d9e5ee2c85ba702dfc77bb80846b41ea8f03e2f489a474ae7802669`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c13cfb1e457e1db034d3d8dbb41e1ac4441b9265cad815d20d2e18f2fd92b7`  
		Last Modified: Wed, 11 Jun 2025 05:53:42 GMT  
		Size: 49.6 MB (49554691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8913a34ef1b12f14e3def3cfea96e72e91804657555a02d6912c14cfedaf`  
		Last Modified: Wed, 11 Jun 2025 05:12:21 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd53944abf9eecaddc2148601ab23afdaa2b69bb36202fc947bdf17be53bb785`  
		Last Modified: Wed, 11 Jun 2025 05:53:46 GMT  
		Size: 139.8 MB (139775267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:677a33b1639693ad7c00593f0649db746166227b73fc3c02d46ef6f4b91486e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b223d4f7e131718996fe85a74df9696702f4b6303954e3c850d7bef071f99`

```dockerfile
```

-	Layers:
	-	`sha256:187ce532a4b8f6cccdf13506fddd3895ff978429e3c48678d152c510ab6ad705`  
		Last Modified: Wed, 11 Jun 2025 05:53:21 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d6ed60b5592e5b5aeca5b75b430bbff8b6200dc67acde5ce36a014081feb0100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284470325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477da2cbe6abbdecbd86c008705533cad11f1d8cf252de27df49cd851e86710f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f7366910d5162a8454b8cd609374efefd77304102bc57a3cda111b61139a61`  
		Last Modified: Wed, 11 Jun 2025 03:03:11 GMT  
		Size: 54.7 MB (54682785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c5b0c8139e4bf74b24cf62a0a02d49f400e4bbc5532b0c2e4b22c9c1b0a8b`  
		Last Modified: Wed, 11 Jun 2025 03:03:09 GMT  
		Size: 1.5 MB (1488215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4829dd9bfb09111a18d959bf52da79fc90ae1e1f05b45aaae223065d9f26030`  
		Last Modified: Wed, 11 Jun 2025 05:53:39 GMT  
		Size: 200.2 MB (200221618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:304e63e340214c7b274804a791fe847f10955783b6d5fed5e0d3e04afbaf64f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013d3b4f526af46a86bc8dc3c31b93a30c60249c9d0ee012ea9dddb2f3066e0f`

```dockerfile
```

-	Layers:
	-	`sha256:502c952ddb1183ed349b6e2aab646d43d288ffdac0b00e2684f27743c3caff19`  
		Last Modified: Wed, 11 Jun 2025 05:53:24 GMT  
		Size: 19.8 KB (19805 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:50056357ebfe43304527d5c811f537be8e2675f3460b719c6083eb89d2791517
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3-sdk` - linux; amd64

```console
$ docker pull dart@sha256:957afa52747de2fd6222741c0eb3abb06d3aee7b4b042c30eb8fdce32ac69af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285790189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4f3493981e07d7cb55687a8ba0c992f71bab9172c5b4fe555a93709907ad1f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309573cdb83d25db63305504108d32d9c8e4b326521651232684ce334b9ed75d`  
		Last Modified: Tue, 10 Jun 2025 23:37:56 GMT  
		Size: 54.9 MB (54910529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f693390485d0102e4afcc6882973e00e0737029d9b78684e19ab97d7041b3761`  
		Last Modified: Tue, 10 Jun 2025 23:37:53 GMT  
		Size: 1.8 MB (1785451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278953d6a98dbb5b3ae9f0b38fd5faaab6c6cfaa44021397bab7be1281e2d2fb`  
		Last Modified: Wed, 11 Jun 2025 02:53:51 GMT  
		Size: 200.9 MB (200864048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c355799bf4df5cbc2a36ede6a8be2ae9f88b075dcd7eda7eea100fab50febe7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e6bd61dc498fc8e05c902861afb82f2341f7e2482177dae54b01e61fb0a34e`

```dockerfile
```

-	Layers:
	-	`sha256:be3f7a30f8d54b4c070d59c6aaa5b4c18594593c7e38c4ecde8a98b63e0a8450`  
		Last Modified: Wed, 11 Jun 2025 02:53:18 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:0d6c4e08a0df4341ab8754418d43a6df4ebc2059579b9e8ddfb040402f5934b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214490678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9f47c2d9e5ee2c85ba702dfc77bb80846b41ea8f03e2f489a474ae7802669`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c13cfb1e457e1db034d3d8dbb41e1ac4441b9265cad815d20d2e18f2fd92b7`  
		Last Modified: Wed, 11 Jun 2025 05:53:42 GMT  
		Size: 49.6 MB (49554691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8913a34ef1b12f14e3def3cfea96e72e91804657555a02d6912c14cfedaf`  
		Last Modified: Wed, 11 Jun 2025 05:12:21 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd53944abf9eecaddc2148601ab23afdaa2b69bb36202fc947bdf17be53bb785`  
		Last Modified: Wed, 11 Jun 2025 05:53:46 GMT  
		Size: 139.8 MB (139775267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:677a33b1639693ad7c00593f0649db746166227b73fc3c02d46ef6f4b91486e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b223d4f7e131718996fe85a74df9696702f4b6303954e3c850d7bef071f99`

```dockerfile
```

-	Layers:
	-	`sha256:187ce532a4b8f6cccdf13506fddd3895ff978429e3c48678d152c510ab6ad705`  
		Last Modified: Wed, 11 Jun 2025 05:53:21 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d6ed60b5592e5b5aeca5b75b430bbff8b6200dc67acde5ce36a014081feb0100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284470325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477da2cbe6abbdecbd86c008705533cad11f1d8cf252de27df49cd851e86710f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f7366910d5162a8454b8cd609374efefd77304102bc57a3cda111b61139a61`  
		Last Modified: Wed, 11 Jun 2025 03:03:11 GMT  
		Size: 54.7 MB (54682785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c5b0c8139e4bf74b24cf62a0a02d49f400e4bbc5532b0c2e4b22c9c1b0a8b`  
		Last Modified: Wed, 11 Jun 2025 03:03:09 GMT  
		Size: 1.5 MB (1488215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4829dd9bfb09111a18d959bf52da79fc90ae1e1f05b45aaae223065d9f26030`  
		Last Modified: Wed, 11 Jun 2025 05:53:39 GMT  
		Size: 200.2 MB (200221618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:304e63e340214c7b274804a791fe847f10955783b6d5fed5e0d3e04afbaf64f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013d3b4f526af46a86bc8dc3c31b93a30c60249c9d0ee012ea9dddb2f3066e0f`

```dockerfile
```

-	Layers:
	-	`sha256:502c952ddb1183ed349b6e2aab646d43d288ffdac0b00e2684f27743c3caff19`  
		Last Modified: Wed, 11 Jun 2025 05:53:24 GMT  
		Size: 19.8 KB (19805 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8`

```console
$ docker pull dart@sha256:50056357ebfe43304527d5c811f537be8e2675f3460b719c6083eb89d2791517
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.8` - linux; amd64

```console
$ docker pull dart@sha256:957afa52747de2fd6222741c0eb3abb06d3aee7b4b042c30eb8fdce32ac69af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285790189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4f3493981e07d7cb55687a8ba0c992f71bab9172c5b4fe555a93709907ad1f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309573cdb83d25db63305504108d32d9c8e4b326521651232684ce334b9ed75d`  
		Last Modified: Tue, 10 Jun 2025 23:37:56 GMT  
		Size: 54.9 MB (54910529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f693390485d0102e4afcc6882973e00e0737029d9b78684e19ab97d7041b3761`  
		Last Modified: Tue, 10 Jun 2025 23:37:53 GMT  
		Size: 1.8 MB (1785451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278953d6a98dbb5b3ae9f0b38fd5faaab6c6cfaa44021397bab7be1281e2d2fb`  
		Last Modified: Wed, 11 Jun 2025 02:53:51 GMT  
		Size: 200.9 MB (200864048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8` - unknown; unknown

```console
$ docker pull dart@sha256:c355799bf4df5cbc2a36ede6a8be2ae9f88b075dcd7eda7eea100fab50febe7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e6bd61dc498fc8e05c902861afb82f2341f7e2482177dae54b01e61fb0a34e`

```dockerfile
```

-	Layers:
	-	`sha256:be3f7a30f8d54b4c070d59c6aaa5b4c18594593c7e38c4ecde8a98b63e0a8450`  
		Last Modified: Wed, 11 Jun 2025 02:53:18 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8` - linux; arm variant v7

```console
$ docker pull dart@sha256:0d6c4e08a0df4341ab8754418d43a6df4ebc2059579b9e8ddfb040402f5934b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214490678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9f47c2d9e5ee2c85ba702dfc77bb80846b41ea8f03e2f489a474ae7802669`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c13cfb1e457e1db034d3d8dbb41e1ac4441b9265cad815d20d2e18f2fd92b7`  
		Last Modified: Wed, 11 Jun 2025 05:53:42 GMT  
		Size: 49.6 MB (49554691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8913a34ef1b12f14e3def3cfea96e72e91804657555a02d6912c14cfedaf`  
		Last Modified: Wed, 11 Jun 2025 05:12:21 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd53944abf9eecaddc2148601ab23afdaa2b69bb36202fc947bdf17be53bb785`  
		Last Modified: Wed, 11 Jun 2025 05:53:46 GMT  
		Size: 139.8 MB (139775267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8` - unknown; unknown

```console
$ docker pull dart@sha256:677a33b1639693ad7c00593f0649db746166227b73fc3c02d46ef6f4b91486e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b223d4f7e131718996fe85a74df9696702f4b6303954e3c850d7bef071f99`

```dockerfile
```

-	Layers:
	-	`sha256:187ce532a4b8f6cccdf13506fddd3895ff978429e3c48678d152c510ab6ad705`  
		Last Modified: Wed, 11 Jun 2025 05:53:21 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d6ed60b5592e5b5aeca5b75b430bbff8b6200dc67acde5ce36a014081feb0100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284470325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477da2cbe6abbdecbd86c008705533cad11f1d8cf252de27df49cd851e86710f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f7366910d5162a8454b8cd609374efefd77304102bc57a3cda111b61139a61`  
		Last Modified: Wed, 11 Jun 2025 03:03:11 GMT  
		Size: 54.7 MB (54682785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c5b0c8139e4bf74b24cf62a0a02d49f400e4bbc5532b0c2e4b22c9c1b0a8b`  
		Last Modified: Wed, 11 Jun 2025 03:03:09 GMT  
		Size: 1.5 MB (1488215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4829dd9bfb09111a18d959bf52da79fc90ae1e1f05b45aaae223065d9f26030`  
		Last Modified: Wed, 11 Jun 2025 05:53:39 GMT  
		Size: 200.2 MB (200221618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8` - unknown; unknown

```console
$ docker pull dart@sha256:304e63e340214c7b274804a791fe847f10955783b6d5fed5e0d3e04afbaf64f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013d3b4f526af46a86bc8dc3c31b93a30c60249c9d0ee012ea9dddb2f3066e0f`

```dockerfile
```

-	Layers:
	-	`sha256:502c952ddb1183ed349b6e2aab646d43d288ffdac0b00e2684f27743c3caff19`  
		Last Modified: Wed, 11 Jun 2025 05:53:24 GMT  
		Size: 19.8 KB (19805 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8-sdk`

```console
$ docker pull dart@sha256:50056357ebfe43304527d5c811f537be8e2675f3460b719c6083eb89d2791517
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.8-sdk` - linux; amd64

```console
$ docker pull dart@sha256:957afa52747de2fd6222741c0eb3abb06d3aee7b4b042c30eb8fdce32ac69af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285790189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4f3493981e07d7cb55687a8ba0c992f71bab9172c5b4fe555a93709907ad1f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309573cdb83d25db63305504108d32d9c8e4b326521651232684ce334b9ed75d`  
		Last Modified: Tue, 10 Jun 2025 23:37:56 GMT  
		Size: 54.9 MB (54910529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f693390485d0102e4afcc6882973e00e0737029d9b78684e19ab97d7041b3761`  
		Last Modified: Tue, 10 Jun 2025 23:37:53 GMT  
		Size: 1.8 MB (1785451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278953d6a98dbb5b3ae9f0b38fd5faaab6c6cfaa44021397bab7be1281e2d2fb`  
		Last Modified: Wed, 11 Jun 2025 02:53:51 GMT  
		Size: 200.9 MB (200864048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c355799bf4df5cbc2a36ede6a8be2ae9f88b075dcd7eda7eea100fab50febe7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e6bd61dc498fc8e05c902861afb82f2341f7e2482177dae54b01e61fb0a34e`

```dockerfile
```

-	Layers:
	-	`sha256:be3f7a30f8d54b4c070d59c6aaa5b4c18594593c7e38c4ecde8a98b63e0a8450`  
		Last Modified: Wed, 11 Jun 2025 02:53:18 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:0d6c4e08a0df4341ab8754418d43a6df4ebc2059579b9e8ddfb040402f5934b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214490678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9f47c2d9e5ee2c85ba702dfc77bb80846b41ea8f03e2f489a474ae7802669`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c13cfb1e457e1db034d3d8dbb41e1ac4441b9265cad815d20d2e18f2fd92b7`  
		Last Modified: Wed, 11 Jun 2025 05:53:42 GMT  
		Size: 49.6 MB (49554691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8913a34ef1b12f14e3def3cfea96e72e91804657555a02d6912c14cfedaf`  
		Last Modified: Wed, 11 Jun 2025 05:12:21 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd53944abf9eecaddc2148601ab23afdaa2b69bb36202fc947bdf17be53bb785`  
		Last Modified: Wed, 11 Jun 2025 05:53:46 GMT  
		Size: 139.8 MB (139775267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:677a33b1639693ad7c00593f0649db746166227b73fc3c02d46ef6f4b91486e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b223d4f7e131718996fe85a74df9696702f4b6303954e3c850d7bef071f99`

```dockerfile
```

-	Layers:
	-	`sha256:187ce532a4b8f6cccdf13506fddd3895ff978429e3c48678d152c510ab6ad705`  
		Last Modified: Wed, 11 Jun 2025 05:53:21 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d6ed60b5592e5b5aeca5b75b430bbff8b6200dc67acde5ce36a014081feb0100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284470325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477da2cbe6abbdecbd86c008705533cad11f1d8cf252de27df49cd851e86710f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f7366910d5162a8454b8cd609374efefd77304102bc57a3cda111b61139a61`  
		Last Modified: Wed, 11 Jun 2025 03:03:11 GMT  
		Size: 54.7 MB (54682785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c5b0c8139e4bf74b24cf62a0a02d49f400e4bbc5532b0c2e4b22c9c1b0a8b`  
		Last Modified: Wed, 11 Jun 2025 03:03:09 GMT  
		Size: 1.5 MB (1488215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4829dd9bfb09111a18d959bf52da79fc90ae1e1f05b45aaae223065d9f26030`  
		Last Modified: Wed, 11 Jun 2025 05:53:39 GMT  
		Size: 200.2 MB (200221618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:304e63e340214c7b274804a791fe847f10955783b6d5fed5e0d3e04afbaf64f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013d3b4f526af46a86bc8dc3c31b93a30c60249c9d0ee012ea9dddb2f3066e0f`

```dockerfile
```

-	Layers:
	-	`sha256:502c952ddb1183ed349b6e2aab646d43d288ffdac0b00e2684f27743c3caff19`  
		Last Modified: Wed, 11 Jun 2025 05:53:24 GMT  
		Size: 19.8 KB (19805 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8.1`

```console
$ docker pull dart@sha256:50056357ebfe43304527d5c811f537be8e2675f3460b719c6083eb89d2791517
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.8.1` - linux; amd64

```console
$ docker pull dart@sha256:957afa52747de2fd6222741c0eb3abb06d3aee7b4b042c30eb8fdce32ac69af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285790189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4f3493981e07d7cb55687a8ba0c992f71bab9172c5b4fe555a93709907ad1f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309573cdb83d25db63305504108d32d9c8e4b326521651232684ce334b9ed75d`  
		Last Modified: Tue, 10 Jun 2025 23:37:56 GMT  
		Size: 54.9 MB (54910529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f693390485d0102e4afcc6882973e00e0737029d9b78684e19ab97d7041b3761`  
		Last Modified: Tue, 10 Jun 2025 23:37:53 GMT  
		Size: 1.8 MB (1785451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278953d6a98dbb5b3ae9f0b38fd5faaab6c6cfaa44021397bab7be1281e2d2fb`  
		Last Modified: Wed, 11 Jun 2025 02:53:51 GMT  
		Size: 200.9 MB (200864048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.1` - unknown; unknown

```console
$ docker pull dart@sha256:c355799bf4df5cbc2a36ede6a8be2ae9f88b075dcd7eda7eea100fab50febe7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e6bd61dc498fc8e05c902861afb82f2341f7e2482177dae54b01e61fb0a34e`

```dockerfile
```

-	Layers:
	-	`sha256:be3f7a30f8d54b4c070d59c6aaa5b4c18594593c7e38c4ecde8a98b63e0a8450`  
		Last Modified: Wed, 11 Jun 2025 02:53:18 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.1` - linux; arm variant v7

```console
$ docker pull dart@sha256:0d6c4e08a0df4341ab8754418d43a6df4ebc2059579b9e8ddfb040402f5934b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214490678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9f47c2d9e5ee2c85ba702dfc77bb80846b41ea8f03e2f489a474ae7802669`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c13cfb1e457e1db034d3d8dbb41e1ac4441b9265cad815d20d2e18f2fd92b7`  
		Last Modified: Wed, 11 Jun 2025 05:53:42 GMT  
		Size: 49.6 MB (49554691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8913a34ef1b12f14e3def3cfea96e72e91804657555a02d6912c14cfedaf`  
		Last Modified: Wed, 11 Jun 2025 05:12:21 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd53944abf9eecaddc2148601ab23afdaa2b69bb36202fc947bdf17be53bb785`  
		Last Modified: Wed, 11 Jun 2025 05:53:46 GMT  
		Size: 139.8 MB (139775267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.1` - unknown; unknown

```console
$ docker pull dart@sha256:677a33b1639693ad7c00593f0649db746166227b73fc3c02d46ef6f4b91486e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b223d4f7e131718996fe85a74df9696702f4b6303954e3c850d7bef071f99`

```dockerfile
```

-	Layers:
	-	`sha256:187ce532a4b8f6cccdf13506fddd3895ff978429e3c48678d152c510ab6ad705`  
		Last Modified: Wed, 11 Jun 2025 05:53:21 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.1` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d6ed60b5592e5b5aeca5b75b430bbff8b6200dc67acde5ce36a014081feb0100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284470325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477da2cbe6abbdecbd86c008705533cad11f1d8cf252de27df49cd851e86710f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f7366910d5162a8454b8cd609374efefd77304102bc57a3cda111b61139a61`  
		Last Modified: Wed, 11 Jun 2025 03:03:11 GMT  
		Size: 54.7 MB (54682785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c5b0c8139e4bf74b24cf62a0a02d49f400e4bbc5532b0c2e4b22c9c1b0a8b`  
		Last Modified: Wed, 11 Jun 2025 03:03:09 GMT  
		Size: 1.5 MB (1488215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4829dd9bfb09111a18d959bf52da79fc90ae1e1f05b45aaae223065d9f26030`  
		Last Modified: Wed, 11 Jun 2025 05:53:39 GMT  
		Size: 200.2 MB (200221618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.1` - unknown; unknown

```console
$ docker pull dart@sha256:304e63e340214c7b274804a791fe847f10955783b6d5fed5e0d3e04afbaf64f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013d3b4f526af46a86bc8dc3c31b93a30c60249c9d0ee012ea9dddb2f3066e0f`

```dockerfile
```

-	Layers:
	-	`sha256:502c952ddb1183ed349b6e2aab646d43d288ffdac0b00e2684f27743c3caff19`  
		Last Modified: Wed, 11 Jun 2025 05:53:24 GMT  
		Size: 19.8 KB (19805 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8.1-sdk`

```console
$ docker pull dart@sha256:50056357ebfe43304527d5c811f537be8e2675f3460b719c6083eb89d2791517
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.8.1-sdk` - linux; amd64

```console
$ docker pull dart@sha256:957afa52747de2fd6222741c0eb3abb06d3aee7b4b042c30eb8fdce32ac69af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285790189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4f3493981e07d7cb55687a8ba0c992f71bab9172c5b4fe555a93709907ad1f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309573cdb83d25db63305504108d32d9c8e4b326521651232684ce334b9ed75d`  
		Last Modified: Tue, 10 Jun 2025 23:37:56 GMT  
		Size: 54.9 MB (54910529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f693390485d0102e4afcc6882973e00e0737029d9b78684e19ab97d7041b3761`  
		Last Modified: Tue, 10 Jun 2025 23:37:53 GMT  
		Size: 1.8 MB (1785451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278953d6a98dbb5b3ae9f0b38fd5faaab6c6cfaa44021397bab7be1281e2d2fb`  
		Last Modified: Wed, 11 Jun 2025 02:53:51 GMT  
		Size: 200.9 MB (200864048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c355799bf4df5cbc2a36ede6a8be2ae9f88b075dcd7eda7eea100fab50febe7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e6bd61dc498fc8e05c902861afb82f2341f7e2482177dae54b01e61fb0a34e`

```dockerfile
```

-	Layers:
	-	`sha256:be3f7a30f8d54b4c070d59c6aaa5b4c18594593c7e38c4ecde8a98b63e0a8450`  
		Last Modified: Wed, 11 Jun 2025 02:53:18 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.1-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:0d6c4e08a0df4341ab8754418d43a6df4ebc2059579b9e8ddfb040402f5934b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214490678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9f47c2d9e5ee2c85ba702dfc77bb80846b41ea8f03e2f489a474ae7802669`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c13cfb1e457e1db034d3d8dbb41e1ac4441b9265cad815d20d2e18f2fd92b7`  
		Last Modified: Wed, 11 Jun 2025 05:53:42 GMT  
		Size: 49.6 MB (49554691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8913a34ef1b12f14e3def3cfea96e72e91804657555a02d6912c14cfedaf`  
		Last Modified: Wed, 11 Jun 2025 05:12:21 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd53944abf9eecaddc2148601ab23afdaa2b69bb36202fc947bdf17be53bb785`  
		Last Modified: Wed, 11 Jun 2025 05:53:46 GMT  
		Size: 139.8 MB (139775267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:677a33b1639693ad7c00593f0649db746166227b73fc3c02d46ef6f4b91486e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b223d4f7e131718996fe85a74df9696702f4b6303954e3c850d7bef071f99`

```dockerfile
```

-	Layers:
	-	`sha256:187ce532a4b8f6cccdf13506fddd3895ff978429e3c48678d152c510ab6ad705`  
		Last Modified: Wed, 11 Jun 2025 05:53:21 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.1-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d6ed60b5592e5b5aeca5b75b430bbff8b6200dc67acde5ce36a014081feb0100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284470325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477da2cbe6abbdecbd86c008705533cad11f1d8cf252de27df49cd851e86710f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f7366910d5162a8454b8cd609374efefd77304102bc57a3cda111b61139a61`  
		Last Modified: Wed, 11 Jun 2025 03:03:11 GMT  
		Size: 54.7 MB (54682785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c5b0c8139e4bf74b24cf62a0a02d49f400e4bbc5532b0c2e4b22c9c1b0a8b`  
		Last Modified: Wed, 11 Jun 2025 03:03:09 GMT  
		Size: 1.5 MB (1488215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4829dd9bfb09111a18d959bf52da79fc90ae1e1f05b45aaae223065d9f26030`  
		Last Modified: Wed, 11 Jun 2025 05:53:39 GMT  
		Size: 200.2 MB (200221618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:304e63e340214c7b274804a791fe847f10955783b6d5fed5e0d3e04afbaf64f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013d3b4f526af46a86bc8dc3c31b93a30c60249c9d0ee012ea9dddb2f3066e0f`

```dockerfile
```

-	Layers:
	-	`sha256:502c952ddb1183ed349b6e2aab646d43d288ffdac0b00e2684f27743c3caff19`  
		Last Modified: Wed, 11 Jun 2025 05:53:24 GMT  
		Size: 19.8 KB (19805 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9.0-196.1.beta`

```console
$ docker pull dart@sha256:c02901aab99050c93f77db82f724909035845727da036d40f5e8d1191fd1ad4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.9.0-196.1.beta` - linux; amd64

```console
$ docker pull dart@sha256:24049bca4a3e6573dccb47760e8ce2012ddd4ac8c7556104dc406ed4a896f7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.5 MB (304500652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d415f0debc8cdf6ddff18b3cabe04f5e6161998494ac7d075c7fe6766f79617b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d97e026a18428748fc3b4fd7762a6e6b03c44954ba5245d7ebef448832ad3efc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51522ceae050f3d6aeedd6a3702992daa34d8aca6e316ef8c33e46e3a3656ea6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e60b9ffd7b5fe2bbc8ee35c492521ba6bc07c94bac64ae7199ca77df737d61a3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-196.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fd5aab236c38814ff1d2d80a53b7b50060923a56cdccc9c4e58ec9c82f954e`  
		Last Modified: Fri, 20 Jun 2025 18:55:44 GMT  
		Size: 54.9 MB (54920926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca71fc5dcd18e25788c62d1204e57f73120ed42930602c37d5187e536937aa4`  
		Last Modified: Fri, 20 Jun 2025 18:55:41 GMT  
		Size: 1.8 MB (1787569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db9b80d39bda1fbc925488f055572673b1e3082d5ce4c4ec9c3a4fed9c96bc4`  
		Last Modified: Fri, 20 Jun 2025 20:54:00 GMT  
		Size: 219.6 MB (219561996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-196.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:82768b65934ef8d5e105b6f180508056c5d5d8338a5c7667595cb9aee4deab74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f0cff3f92d565b025a19e3ca663180428f155ade55902ded00ca8a64c0e14b`

```dockerfile
```

-	Layers:
	-	`sha256:9fe37144b4a1624ab04ba8dded50ab5002efc4303e8345c39ed2fecbbb410734`  
		Last Modified: Fri, 20 Jun 2025 20:53:27 GMT  
		Size: 17.9 KB (17910 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.0-196.1.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:3236e1e7e8764b0e7050ed16d9dea57a1df669e9c534970efd538382ebd1b3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228495385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed524c81192289769ee334fb09313a0c46a73de3943d80e756157a292c47bab0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d97e026a18428748fc3b4fd7762a6e6b03c44954ba5245d7ebef448832ad3efc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51522ceae050f3d6aeedd6a3702992daa34d8aca6e316ef8c33e46e3a3656ea6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e60b9ffd7b5fe2bbc8ee35c492521ba6bc07c94bac64ae7199ca77df737d61a3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-196.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91b5445b5cd74396ae398266097364c0789e065f5d63837e18fdabb4c59b0cb`  
		Last Modified: Fri, 20 Jun 2025 18:55:42 GMT  
		Size: 49.6 MB (49559425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffb13dcfc43925f43218d3c69a9e1dae1baa9b3a09f39e988de50ca0c874616`  
		Last Modified: Fri, 20 Jun 2025 18:55:34 GMT  
		Size: 1.2 MB (1224883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cfdf86d4d8c1745e6df8271c6306284b455ce14ac13427517532ada8018659`  
		Last Modified: Fri, 20 Jun 2025 20:53:53 GMT  
		Size: 153.8 MB (153772301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-196.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:bbab9c42787843b1f3691f9b8c5f0d4859b869edcd730cb8bebd407c92b46944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6c4a847f94d1882895eefa04010a6f3a0341dda5fdc05157e59826b29523d7`

```dockerfile
```

-	Layers:
	-	`sha256:bc177005bdd640ce7a1ee92cb4d47b49e785f38b00cc7a02f604a2d930fc3ebf`  
		Last Modified: Fri, 20 Jun 2025 20:53:31 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.0-196.1.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:90a9a74ad42b3287e38c492f224c7878fdaea5821594541f0cb27d3e52d7a7b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303242520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77b83fb58566b929f1dcc3d697e5800ee35bc4e934554f432460b537344c651`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d97e026a18428748fc3b4fd7762a6e6b03c44954ba5245d7ebef448832ad3efc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51522ceae050f3d6aeedd6a3702992daa34d8aca6e316ef8c33e46e3a3656ea6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e60b9ffd7b5fe2bbc8ee35c492521ba6bc07c94bac64ae7199ca77df737d61a3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-196.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a99f71be7a4940cf0717b24816e206eed540f4f47907f2fe2d5e08d79159807`  
		Last Modified: Fri, 20 Jun 2025 18:55:42 GMT  
		Size: 54.7 MB (54683577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59c5ebfc29b4e3a0740ccbbc037fa1aa72406df574261eddb34c659b54bec8d`  
		Last Modified: Fri, 20 Jun 2025 18:55:33 GMT  
		Size: 1.5 MB (1491209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f157b547212154db62c57fd846fa0deffcc50838d6a110a90ecc75fa60eb3116`  
		Last Modified: Fri, 20 Jun 2025 20:54:31 GMT  
		Size: 219.0 MB (218990027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-196.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:64cb1f5a9ddad43ac59f38a4936233486c83d6f9308b7d17046a36da45c16369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4cd1ba3b76c1363a9e97938dc66be18d42dab8ae25211974f8c51f1c8ca7cac`

```dockerfile
```

-	Layers:
	-	`sha256:2cdfeb6fc4476a4dd69e22058266bf2cf9be3d7d108af353408e2cad7ae6da89`  
		Last Modified: Fri, 20 Jun 2025 20:53:34 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9.0-196.1.beta-sdk`

```console
$ docker pull dart@sha256:c02901aab99050c93f77db82f724909035845727da036d40f5e8d1191fd1ad4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.9.0-196.1.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:24049bca4a3e6573dccb47760e8ce2012ddd4ac8c7556104dc406ed4a896f7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.5 MB (304500652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d415f0debc8cdf6ddff18b3cabe04f5e6161998494ac7d075c7fe6766f79617b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d97e026a18428748fc3b4fd7762a6e6b03c44954ba5245d7ebef448832ad3efc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51522ceae050f3d6aeedd6a3702992daa34d8aca6e316ef8c33e46e3a3656ea6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e60b9ffd7b5fe2bbc8ee35c492521ba6bc07c94bac64ae7199ca77df737d61a3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-196.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fd5aab236c38814ff1d2d80a53b7b50060923a56cdccc9c4e58ec9c82f954e`  
		Last Modified: Fri, 20 Jun 2025 18:55:44 GMT  
		Size: 54.9 MB (54920926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca71fc5dcd18e25788c62d1204e57f73120ed42930602c37d5187e536937aa4`  
		Last Modified: Fri, 20 Jun 2025 18:55:41 GMT  
		Size: 1.8 MB (1787569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db9b80d39bda1fbc925488f055572673b1e3082d5ce4c4ec9c3a4fed9c96bc4`  
		Last Modified: Fri, 20 Jun 2025 20:54:00 GMT  
		Size: 219.6 MB (219561996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-196.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:82768b65934ef8d5e105b6f180508056c5d5d8338a5c7667595cb9aee4deab74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f0cff3f92d565b025a19e3ca663180428f155ade55902ded00ca8a64c0e14b`

```dockerfile
```

-	Layers:
	-	`sha256:9fe37144b4a1624ab04ba8dded50ab5002efc4303e8345c39ed2fecbbb410734`  
		Last Modified: Fri, 20 Jun 2025 20:53:27 GMT  
		Size: 17.9 KB (17910 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.0-196.1.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:3236e1e7e8764b0e7050ed16d9dea57a1df669e9c534970efd538382ebd1b3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228495385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed524c81192289769ee334fb09313a0c46a73de3943d80e756157a292c47bab0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d97e026a18428748fc3b4fd7762a6e6b03c44954ba5245d7ebef448832ad3efc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51522ceae050f3d6aeedd6a3702992daa34d8aca6e316ef8c33e46e3a3656ea6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e60b9ffd7b5fe2bbc8ee35c492521ba6bc07c94bac64ae7199ca77df737d61a3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-196.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91b5445b5cd74396ae398266097364c0789e065f5d63837e18fdabb4c59b0cb`  
		Last Modified: Fri, 20 Jun 2025 18:55:42 GMT  
		Size: 49.6 MB (49559425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffb13dcfc43925f43218d3c69a9e1dae1baa9b3a09f39e988de50ca0c874616`  
		Last Modified: Fri, 20 Jun 2025 18:55:34 GMT  
		Size: 1.2 MB (1224883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cfdf86d4d8c1745e6df8271c6306284b455ce14ac13427517532ada8018659`  
		Last Modified: Fri, 20 Jun 2025 20:53:53 GMT  
		Size: 153.8 MB (153772301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-196.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:bbab9c42787843b1f3691f9b8c5f0d4859b869edcd730cb8bebd407c92b46944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6c4a847f94d1882895eefa04010a6f3a0341dda5fdc05157e59826b29523d7`

```dockerfile
```

-	Layers:
	-	`sha256:bc177005bdd640ce7a1ee92cb4d47b49e785f38b00cc7a02f604a2d930fc3ebf`  
		Last Modified: Fri, 20 Jun 2025 20:53:31 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.0-196.1.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:90a9a74ad42b3287e38c492f224c7878fdaea5821594541f0cb27d3e52d7a7b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303242520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77b83fb58566b929f1dcc3d697e5800ee35bc4e934554f432460b537344c651`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d97e026a18428748fc3b4fd7762a6e6b03c44954ba5245d7ebef448832ad3efc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51522ceae050f3d6aeedd6a3702992daa34d8aca6e316ef8c33e46e3a3656ea6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e60b9ffd7b5fe2bbc8ee35c492521ba6bc07c94bac64ae7199ca77df737d61a3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-196.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a99f71be7a4940cf0717b24816e206eed540f4f47907f2fe2d5e08d79159807`  
		Last Modified: Fri, 20 Jun 2025 18:55:42 GMT  
		Size: 54.7 MB (54683577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59c5ebfc29b4e3a0740ccbbc037fa1aa72406df574261eddb34c659b54bec8d`  
		Last Modified: Fri, 20 Jun 2025 18:55:33 GMT  
		Size: 1.5 MB (1491209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f157b547212154db62c57fd846fa0deffcc50838d6a110a90ecc75fa60eb3116`  
		Last Modified: Fri, 20 Jun 2025 20:54:31 GMT  
		Size: 219.0 MB (218990027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-196.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:64cb1f5a9ddad43ac59f38a4936233486c83d6f9308b7d17046a36da45c16369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4cd1ba3b76c1363a9e97938dc66be18d42dab8ae25211974f8c51f1c8ca7cac`

```dockerfile
```

-	Layers:
	-	`sha256:2cdfeb6fc4476a4dd69e22058266bf2cf9be3d7d108af353408e2cad7ae6da89`  
		Last Modified: Fri, 20 Jun 2025 20:53:34 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:c02901aab99050c93f77db82f724909035845727da036d40f5e8d1191fd1ad4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:24049bca4a3e6573dccb47760e8ce2012ddd4ac8c7556104dc406ed4a896f7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.5 MB (304500652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d415f0debc8cdf6ddff18b3cabe04f5e6161998494ac7d075c7fe6766f79617b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d97e026a18428748fc3b4fd7762a6e6b03c44954ba5245d7ebef448832ad3efc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51522ceae050f3d6aeedd6a3702992daa34d8aca6e316ef8c33e46e3a3656ea6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e60b9ffd7b5fe2bbc8ee35c492521ba6bc07c94bac64ae7199ca77df737d61a3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-196.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fd5aab236c38814ff1d2d80a53b7b50060923a56cdccc9c4e58ec9c82f954e`  
		Last Modified: Fri, 20 Jun 2025 18:55:44 GMT  
		Size: 54.9 MB (54920926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca71fc5dcd18e25788c62d1204e57f73120ed42930602c37d5187e536937aa4`  
		Last Modified: Fri, 20 Jun 2025 18:55:41 GMT  
		Size: 1.8 MB (1787569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db9b80d39bda1fbc925488f055572673b1e3082d5ce4c4ec9c3a4fed9c96bc4`  
		Last Modified: Fri, 20 Jun 2025 20:54:00 GMT  
		Size: 219.6 MB (219561996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:82768b65934ef8d5e105b6f180508056c5d5d8338a5c7667595cb9aee4deab74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f0cff3f92d565b025a19e3ca663180428f155ade55902ded00ca8a64c0e14b`

```dockerfile
```

-	Layers:
	-	`sha256:9fe37144b4a1624ab04ba8dded50ab5002efc4303e8345c39ed2fecbbb410734`  
		Last Modified: Fri, 20 Jun 2025 20:53:27 GMT  
		Size: 17.9 KB (17910 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:3236e1e7e8764b0e7050ed16d9dea57a1df669e9c534970efd538382ebd1b3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228495385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed524c81192289769ee334fb09313a0c46a73de3943d80e756157a292c47bab0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d97e026a18428748fc3b4fd7762a6e6b03c44954ba5245d7ebef448832ad3efc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51522ceae050f3d6aeedd6a3702992daa34d8aca6e316ef8c33e46e3a3656ea6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e60b9ffd7b5fe2bbc8ee35c492521ba6bc07c94bac64ae7199ca77df737d61a3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-196.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91b5445b5cd74396ae398266097364c0789e065f5d63837e18fdabb4c59b0cb`  
		Last Modified: Fri, 20 Jun 2025 18:55:42 GMT  
		Size: 49.6 MB (49559425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffb13dcfc43925f43218d3c69a9e1dae1baa9b3a09f39e988de50ca0c874616`  
		Last Modified: Fri, 20 Jun 2025 18:55:34 GMT  
		Size: 1.2 MB (1224883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cfdf86d4d8c1745e6df8271c6306284b455ce14ac13427517532ada8018659`  
		Last Modified: Fri, 20 Jun 2025 20:53:53 GMT  
		Size: 153.8 MB (153772301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:bbab9c42787843b1f3691f9b8c5f0d4859b869edcd730cb8bebd407c92b46944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6c4a847f94d1882895eefa04010a6f3a0341dda5fdc05157e59826b29523d7`

```dockerfile
```

-	Layers:
	-	`sha256:bc177005bdd640ce7a1ee92cb4d47b49e785f38b00cc7a02f604a2d930fc3ebf`  
		Last Modified: Fri, 20 Jun 2025 20:53:31 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:90a9a74ad42b3287e38c492f224c7878fdaea5821594541f0cb27d3e52d7a7b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303242520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77b83fb58566b929f1dcc3d697e5800ee35bc4e934554f432460b537344c651`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d97e026a18428748fc3b4fd7762a6e6b03c44954ba5245d7ebef448832ad3efc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51522ceae050f3d6aeedd6a3702992daa34d8aca6e316ef8c33e46e3a3656ea6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e60b9ffd7b5fe2bbc8ee35c492521ba6bc07c94bac64ae7199ca77df737d61a3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-196.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a99f71be7a4940cf0717b24816e206eed540f4f47907f2fe2d5e08d79159807`  
		Last Modified: Fri, 20 Jun 2025 18:55:42 GMT  
		Size: 54.7 MB (54683577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59c5ebfc29b4e3a0740ccbbc037fa1aa72406df574261eddb34c659b54bec8d`  
		Last Modified: Fri, 20 Jun 2025 18:55:33 GMT  
		Size: 1.5 MB (1491209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f157b547212154db62c57fd846fa0deffcc50838d6a110a90ecc75fa60eb3116`  
		Last Modified: Fri, 20 Jun 2025 20:54:31 GMT  
		Size: 219.0 MB (218990027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:64cb1f5a9ddad43ac59f38a4936233486c83d6f9308b7d17046a36da45c16369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4cd1ba3b76c1363a9e97938dc66be18d42dab8ae25211974f8c51f1c8ca7cac`

```dockerfile
```

-	Layers:
	-	`sha256:2cdfeb6fc4476a4dd69e22058266bf2cf9be3d7d108af353408e2cad7ae6da89`  
		Last Modified: Fri, 20 Jun 2025 20:53:34 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:c02901aab99050c93f77db82f724909035845727da036d40f5e8d1191fd1ad4e
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
$ docker pull dart@sha256:24049bca4a3e6573dccb47760e8ce2012ddd4ac8c7556104dc406ed4a896f7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.5 MB (304500652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d415f0debc8cdf6ddff18b3cabe04f5e6161998494ac7d075c7fe6766f79617b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d97e026a18428748fc3b4fd7762a6e6b03c44954ba5245d7ebef448832ad3efc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51522ceae050f3d6aeedd6a3702992daa34d8aca6e316ef8c33e46e3a3656ea6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e60b9ffd7b5fe2bbc8ee35c492521ba6bc07c94bac64ae7199ca77df737d61a3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-196.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fd5aab236c38814ff1d2d80a53b7b50060923a56cdccc9c4e58ec9c82f954e`  
		Last Modified: Fri, 20 Jun 2025 18:55:44 GMT  
		Size: 54.9 MB (54920926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca71fc5dcd18e25788c62d1204e57f73120ed42930602c37d5187e536937aa4`  
		Last Modified: Fri, 20 Jun 2025 18:55:41 GMT  
		Size: 1.8 MB (1787569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db9b80d39bda1fbc925488f055572673b1e3082d5ce4c4ec9c3a4fed9c96bc4`  
		Last Modified: Fri, 20 Jun 2025 20:54:00 GMT  
		Size: 219.6 MB (219561996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:82768b65934ef8d5e105b6f180508056c5d5d8338a5c7667595cb9aee4deab74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f0cff3f92d565b025a19e3ca663180428f155ade55902ded00ca8a64c0e14b`

```dockerfile
```

-	Layers:
	-	`sha256:9fe37144b4a1624ab04ba8dded50ab5002efc4303e8345c39ed2fecbbb410734`  
		Last Modified: Fri, 20 Jun 2025 20:53:27 GMT  
		Size: 17.9 KB (17910 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:3236e1e7e8764b0e7050ed16d9dea57a1df669e9c534970efd538382ebd1b3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228495385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed524c81192289769ee334fb09313a0c46a73de3943d80e756157a292c47bab0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d97e026a18428748fc3b4fd7762a6e6b03c44954ba5245d7ebef448832ad3efc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51522ceae050f3d6aeedd6a3702992daa34d8aca6e316ef8c33e46e3a3656ea6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e60b9ffd7b5fe2bbc8ee35c492521ba6bc07c94bac64ae7199ca77df737d61a3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-196.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91b5445b5cd74396ae398266097364c0789e065f5d63837e18fdabb4c59b0cb`  
		Last Modified: Fri, 20 Jun 2025 18:55:42 GMT  
		Size: 49.6 MB (49559425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffb13dcfc43925f43218d3c69a9e1dae1baa9b3a09f39e988de50ca0c874616`  
		Last Modified: Fri, 20 Jun 2025 18:55:34 GMT  
		Size: 1.2 MB (1224883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cfdf86d4d8c1745e6df8271c6306284b455ce14ac13427517532ada8018659`  
		Last Modified: Fri, 20 Jun 2025 20:53:53 GMT  
		Size: 153.8 MB (153772301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:bbab9c42787843b1f3691f9b8c5f0d4859b869edcd730cb8bebd407c92b46944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6c4a847f94d1882895eefa04010a6f3a0341dda5fdc05157e59826b29523d7`

```dockerfile
```

-	Layers:
	-	`sha256:bc177005bdd640ce7a1ee92cb4d47b49e785f38b00cc7a02f604a2d930fc3ebf`  
		Last Modified: Fri, 20 Jun 2025 20:53:31 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:90a9a74ad42b3287e38c492f224c7878fdaea5821594541f0cb27d3e52d7a7b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303242520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77b83fb58566b929f1dcc3d697e5800ee35bc4e934554f432460b537344c651`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Jun 2025 07:46:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 04 Jun 2025 07:46:12 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Jun 2025 07:46:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 07:46:12 GMT
WORKDIR /root
# Wed, 04 Jun 2025 07:46:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d97e026a18428748fc3b4fd7762a6e6b03c44954ba5245d7ebef448832ad3efc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51522ceae050f3d6aeedd6a3702992daa34d8aca6e316ef8c33e46e3a3656ea6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e60b9ffd7b5fe2bbc8ee35c492521ba6bc07c94bac64ae7199ca77df737d61a3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-196.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a99f71be7a4940cf0717b24816e206eed540f4f47907f2fe2d5e08d79159807`  
		Last Modified: Fri, 20 Jun 2025 18:55:42 GMT  
		Size: 54.7 MB (54683577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59c5ebfc29b4e3a0740ccbbc037fa1aa72406df574261eddb34c659b54bec8d`  
		Last Modified: Fri, 20 Jun 2025 18:55:33 GMT  
		Size: 1.5 MB (1491209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f157b547212154db62c57fd846fa0deffcc50838d6a110a90ecc75fa60eb3116`  
		Last Modified: Fri, 20 Jun 2025 20:54:31 GMT  
		Size: 219.0 MB (218990027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:64cb1f5a9ddad43ac59f38a4936233486c83d6f9308b7d17046a36da45c16369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4cd1ba3b76c1363a9e97938dc66be18d42dab8ae25211974f8c51f1c8ca7cac`

```dockerfile
```

-	Layers:
	-	`sha256:2cdfeb6fc4476a4dd69e22058266bf2cf9be3d7d108af353408e2cad7ae6da89`  
		Last Modified: Fri, 20 Jun 2025 20:53:34 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:50056357ebfe43304527d5c811f537be8e2675f3460b719c6083eb89d2791517
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:957afa52747de2fd6222741c0eb3abb06d3aee7b4b042c30eb8fdce32ac69af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285790189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4f3493981e07d7cb55687a8ba0c992f71bab9172c5b4fe555a93709907ad1f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309573cdb83d25db63305504108d32d9c8e4b326521651232684ce334b9ed75d`  
		Last Modified: Tue, 10 Jun 2025 23:37:56 GMT  
		Size: 54.9 MB (54910529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f693390485d0102e4afcc6882973e00e0737029d9b78684e19ab97d7041b3761`  
		Last Modified: Tue, 10 Jun 2025 23:37:53 GMT  
		Size: 1.8 MB (1785451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278953d6a98dbb5b3ae9f0b38fd5faaab6c6cfaa44021397bab7be1281e2d2fb`  
		Last Modified: Wed, 11 Jun 2025 02:53:51 GMT  
		Size: 200.9 MB (200864048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:c355799bf4df5cbc2a36ede6a8be2ae9f88b075dcd7eda7eea100fab50febe7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e6bd61dc498fc8e05c902861afb82f2341f7e2482177dae54b01e61fb0a34e`

```dockerfile
```

-	Layers:
	-	`sha256:be3f7a30f8d54b4c070d59c6aaa5b4c18594593c7e38c4ecde8a98b63e0a8450`  
		Last Modified: Wed, 11 Jun 2025 02:53:18 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:0d6c4e08a0df4341ab8754418d43a6df4ebc2059579b9e8ddfb040402f5934b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214490678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9f47c2d9e5ee2c85ba702dfc77bb80846b41ea8f03e2f489a474ae7802669`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c13cfb1e457e1db034d3d8dbb41e1ac4441b9265cad815d20d2e18f2fd92b7`  
		Last Modified: Wed, 11 Jun 2025 05:53:42 GMT  
		Size: 49.6 MB (49554691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8913a34ef1b12f14e3def3cfea96e72e91804657555a02d6912c14cfedaf`  
		Last Modified: Wed, 11 Jun 2025 05:12:21 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd53944abf9eecaddc2148601ab23afdaa2b69bb36202fc947bdf17be53bb785`  
		Last Modified: Wed, 11 Jun 2025 05:53:46 GMT  
		Size: 139.8 MB (139775267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:677a33b1639693ad7c00593f0649db746166227b73fc3c02d46ef6f4b91486e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b223d4f7e131718996fe85a74df9696702f4b6303954e3c850d7bef071f99`

```dockerfile
```

-	Layers:
	-	`sha256:187ce532a4b8f6cccdf13506fddd3895ff978429e3c48678d152c510ab6ad705`  
		Last Modified: Wed, 11 Jun 2025 05:53:21 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d6ed60b5592e5b5aeca5b75b430bbff8b6200dc67acde5ce36a014081feb0100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284470325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477da2cbe6abbdecbd86c008705533cad11f1d8cf252de27df49cd851e86710f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f7366910d5162a8454b8cd609374efefd77304102bc57a3cda111b61139a61`  
		Last Modified: Wed, 11 Jun 2025 03:03:11 GMT  
		Size: 54.7 MB (54682785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c5b0c8139e4bf74b24cf62a0a02d49f400e4bbc5532b0c2e4b22c9c1b0a8b`  
		Last Modified: Wed, 11 Jun 2025 03:03:09 GMT  
		Size: 1.5 MB (1488215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4829dd9bfb09111a18d959bf52da79fc90ae1e1f05b45aaae223065d9f26030`  
		Last Modified: Wed, 11 Jun 2025 05:53:39 GMT  
		Size: 200.2 MB (200221618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:304e63e340214c7b274804a791fe847f10955783b6d5fed5e0d3e04afbaf64f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013d3b4f526af46a86bc8dc3c31b93a30c60249c9d0ee012ea9dddb2f3066e0f`

```dockerfile
```

-	Layers:
	-	`sha256:502c952ddb1183ed349b6e2aab646d43d288ffdac0b00e2684f27743c3caff19`  
		Last Modified: Wed, 11 Jun 2025 05:53:24 GMT  
		Size: 19.8 KB (19805 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:50056357ebfe43304527d5c811f537be8e2675f3460b719c6083eb89d2791517
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:957afa52747de2fd6222741c0eb3abb06d3aee7b4b042c30eb8fdce32ac69af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285790189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4f3493981e07d7cb55687a8ba0c992f71bab9172c5b4fe555a93709907ad1f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309573cdb83d25db63305504108d32d9c8e4b326521651232684ce334b9ed75d`  
		Last Modified: Tue, 10 Jun 2025 23:37:56 GMT  
		Size: 54.9 MB (54910529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f693390485d0102e4afcc6882973e00e0737029d9b78684e19ab97d7041b3761`  
		Last Modified: Tue, 10 Jun 2025 23:37:53 GMT  
		Size: 1.8 MB (1785451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278953d6a98dbb5b3ae9f0b38fd5faaab6c6cfaa44021397bab7be1281e2d2fb`  
		Last Modified: Wed, 11 Jun 2025 02:53:51 GMT  
		Size: 200.9 MB (200864048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c355799bf4df5cbc2a36ede6a8be2ae9f88b075dcd7eda7eea100fab50febe7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e6bd61dc498fc8e05c902861afb82f2341f7e2482177dae54b01e61fb0a34e`

```dockerfile
```

-	Layers:
	-	`sha256:be3f7a30f8d54b4c070d59c6aaa5b4c18594593c7e38c4ecde8a98b63e0a8450`  
		Last Modified: Wed, 11 Jun 2025 02:53:18 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:0d6c4e08a0df4341ab8754418d43a6df4ebc2059579b9e8ddfb040402f5934b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214490678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9f47c2d9e5ee2c85ba702dfc77bb80846b41ea8f03e2f489a474ae7802669`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c13cfb1e457e1db034d3d8dbb41e1ac4441b9265cad815d20d2e18f2fd92b7`  
		Last Modified: Wed, 11 Jun 2025 05:53:42 GMT  
		Size: 49.6 MB (49554691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8913a34ef1b12f14e3def3cfea96e72e91804657555a02d6912c14cfedaf`  
		Last Modified: Wed, 11 Jun 2025 05:12:21 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd53944abf9eecaddc2148601ab23afdaa2b69bb36202fc947bdf17be53bb785`  
		Last Modified: Wed, 11 Jun 2025 05:53:46 GMT  
		Size: 139.8 MB (139775267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:677a33b1639693ad7c00593f0649db746166227b73fc3c02d46ef6f4b91486e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b223d4f7e131718996fe85a74df9696702f4b6303954e3c850d7bef071f99`

```dockerfile
```

-	Layers:
	-	`sha256:187ce532a4b8f6cccdf13506fddd3895ff978429e3c48678d152c510ab6ad705`  
		Last Modified: Wed, 11 Jun 2025 05:53:21 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d6ed60b5592e5b5aeca5b75b430bbff8b6200dc67acde5ce36a014081feb0100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284470325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477da2cbe6abbdecbd86c008705533cad11f1d8cf252de27df49cd851e86710f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f7366910d5162a8454b8cd609374efefd77304102bc57a3cda111b61139a61`  
		Last Modified: Wed, 11 Jun 2025 03:03:11 GMT  
		Size: 54.7 MB (54682785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c5b0c8139e4bf74b24cf62a0a02d49f400e4bbc5532b0c2e4b22c9c1b0a8b`  
		Last Modified: Wed, 11 Jun 2025 03:03:09 GMT  
		Size: 1.5 MB (1488215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4829dd9bfb09111a18d959bf52da79fc90ae1e1f05b45aaae223065d9f26030`  
		Last Modified: Wed, 11 Jun 2025 05:53:39 GMT  
		Size: 200.2 MB (200221618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:304e63e340214c7b274804a791fe847f10955783b6d5fed5e0d3e04afbaf64f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013d3b4f526af46a86bc8dc3c31b93a30c60249c9d0ee012ea9dddb2f3066e0f`

```dockerfile
```

-	Layers:
	-	`sha256:502c952ddb1183ed349b6e2aab646d43d288ffdac0b00e2684f27743c3caff19`  
		Last Modified: Wed, 11 Jun 2025 05:53:24 GMT  
		Size: 19.8 KB (19805 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:50056357ebfe43304527d5c811f537be8e2675f3460b719c6083eb89d2791517
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:957afa52747de2fd6222741c0eb3abb06d3aee7b4b042c30eb8fdce32ac69af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285790189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4f3493981e07d7cb55687a8ba0c992f71bab9172c5b4fe555a93709907ad1f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309573cdb83d25db63305504108d32d9c8e4b326521651232684ce334b9ed75d`  
		Last Modified: Tue, 10 Jun 2025 23:37:56 GMT  
		Size: 54.9 MB (54910529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f693390485d0102e4afcc6882973e00e0737029d9b78684e19ab97d7041b3761`  
		Last Modified: Tue, 10 Jun 2025 23:37:53 GMT  
		Size: 1.8 MB (1785451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278953d6a98dbb5b3ae9f0b38fd5faaab6c6cfaa44021397bab7be1281e2d2fb`  
		Last Modified: Wed, 11 Jun 2025 02:53:51 GMT  
		Size: 200.9 MB (200864048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:c355799bf4df5cbc2a36ede6a8be2ae9f88b075dcd7eda7eea100fab50febe7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e6bd61dc498fc8e05c902861afb82f2341f7e2482177dae54b01e61fb0a34e`

```dockerfile
```

-	Layers:
	-	`sha256:be3f7a30f8d54b4c070d59c6aaa5b4c18594593c7e38c4ecde8a98b63e0a8450`  
		Last Modified: Wed, 11 Jun 2025 02:53:18 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:0d6c4e08a0df4341ab8754418d43a6df4ebc2059579b9e8ddfb040402f5934b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214490678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9f47c2d9e5ee2c85ba702dfc77bb80846b41ea8f03e2f489a474ae7802669`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c13cfb1e457e1db034d3d8dbb41e1ac4441b9265cad815d20d2e18f2fd92b7`  
		Last Modified: Wed, 11 Jun 2025 05:53:42 GMT  
		Size: 49.6 MB (49554691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8913a34ef1b12f14e3def3cfea96e72e91804657555a02d6912c14cfedaf`  
		Last Modified: Wed, 11 Jun 2025 05:12:21 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd53944abf9eecaddc2148601ab23afdaa2b69bb36202fc947bdf17be53bb785`  
		Last Modified: Wed, 11 Jun 2025 05:53:46 GMT  
		Size: 139.8 MB (139775267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:677a33b1639693ad7c00593f0649db746166227b73fc3c02d46ef6f4b91486e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b223d4f7e131718996fe85a74df9696702f4b6303954e3c850d7bef071f99`

```dockerfile
```

-	Layers:
	-	`sha256:187ce532a4b8f6cccdf13506fddd3895ff978429e3c48678d152c510ab6ad705`  
		Last Modified: Wed, 11 Jun 2025 05:53:21 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d6ed60b5592e5b5aeca5b75b430bbff8b6200dc67acde5ce36a014081feb0100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284470325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477da2cbe6abbdecbd86c008705533cad11f1d8cf252de27df49cd851e86710f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f7366910d5162a8454b8cd609374efefd77304102bc57a3cda111b61139a61`  
		Last Modified: Wed, 11 Jun 2025 03:03:11 GMT  
		Size: 54.7 MB (54682785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c5b0c8139e4bf74b24cf62a0a02d49f400e4bbc5532b0c2e4b22c9c1b0a8b`  
		Last Modified: Wed, 11 Jun 2025 03:03:09 GMT  
		Size: 1.5 MB (1488215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4829dd9bfb09111a18d959bf52da79fc90ae1e1f05b45aaae223065d9f26030`  
		Last Modified: Wed, 11 Jun 2025 05:53:39 GMT  
		Size: 200.2 MB (200221618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:304e63e340214c7b274804a791fe847f10955783b6d5fed5e0d3e04afbaf64f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013d3b4f526af46a86bc8dc3c31b93a30c60249c9d0ee012ea9dddb2f3066e0f`

```dockerfile
```

-	Layers:
	-	`sha256:502c952ddb1183ed349b6e2aab646d43d288ffdac0b00e2684f27743c3caff19`  
		Last Modified: Wed, 11 Jun 2025 05:53:24 GMT  
		Size: 19.8 KB (19805 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:50056357ebfe43304527d5c811f537be8e2675f3460b719c6083eb89d2791517
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:957afa52747de2fd6222741c0eb3abb06d3aee7b4b042c30eb8fdce32ac69af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285790189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4f3493981e07d7cb55687a8ba0c992f71bab9172c5b4fe555a93709907ad1f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309573cdb83d25db63305504108d32d9c8e4b326521651232684ce334b9ed75d`  
		Last Modified: Tue, 10 Jun 2025 23:37:56 GMT  
		Size: 54.9 MB (54910529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f693390485d0102e4afcc6882973e00e0737029d9b78684e19ab97d7041b3761`  
		Last Modified: Tue, 10 Jun 2025 23:37:53 GMT  
		Size: 1.8 MB (1785451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278953d6a98dbb5b3ae9f0b38fd5faaab6c6cfaa44021397bab7be1281e2d2fb`  
		Last Modified: Wed, 11 Jun 2025 02:53:51 GMT  
		Size: 200.9 MB (200864048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c355799bf4df5cbc2a36ede6a8be2ae9f88b075dcd7eda7eea100fab50febe7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e6bd61dc498fc8e05c902861afb82f2341f7e2482177dae54b01e61fb0a34e`

```dockerfile
```

-	Layers:
	-	`sha256:be3f7a30f8d54b4c070d59c6aaa5b4c18594593c7e38c4ecde8a98b63e0a8450`  
		Last Modified: Wed, 11 Jun 2025 02:53:18 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:0d6c4e08a0df4341ab8754418d43a6df4ebc2059579b9e8ddfb040402f5934b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214490678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9f47c2d9e5ee2c85ba702dfc77bb80846b41ea8f03e2f489a474ae7802669`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c13cfb1e457e1db034d3d8dbb41e1ac4441b9265cad815d20d2e18f2fd92b7`  
		Last Modified: Wed, 11 Jun 2025 05:53:42 GMT  
		Size: 49.6 MB (49554691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8913a34ef1b12f14e3def3cfea96e72e91804657555a02d6912c14cfedaf`  
		Last Modified: Wed, 11 Jun 2025 05:12:21 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd53944abf9eecaddc2148601ab23afdaa2b69bb36202fc947bdf17be53bb785`  
		Last Modified: Wed, 11 Jun 2025 05:53:46 GMT  
		Size: 139.8 MB (139775267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:677a33b1639693ad7c00593f0649db746166227b73fc3c02d46ef6f4b91486e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b223d4f7e131718996fe85a74df9696702f4b6303954e3c850d7bef071f99`

```dockerfile
```

-	Layers:
	-	`sha256:187ce532a4b8f6cccdf13506fddd3895ff978429e3c48678d152c510ab6ad705`  
		Last Modified: Wed, 11 Jun 2025 05:53:21 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d6ed60b5592e5b5aeca5b75b430bbff8b6200dc67acde5ce36a014081feb0100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284470325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477da2cbe6abbdecbd86c008705533cad11f1d8cf252de27df49cd851e86710f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 May 2025 10:45:30 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f7366910d5162a8454b8cd609374efefd77304102bc57a3cda111b61139a61`  
		Last Modified: Wed, 11 Jun 2025 03:03:11 GMT  
		Size: 54.7 MB (54682785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c5b0c8139e4bf74b24cf62a0a02d49f400e4bbc5532b0c2e4b22c9c1b0a8b`  
		Last Modified: Wed, 11 Jun 2025 03:03:09 GMT  
		Size: 1.5 MB (1488215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4829dd9bfb09111a18d959bf52da79fc90ae1e1f05b45aaae223065d9f26030`  
		Last Modified: Wed, 11 Jun 2025 05:53:39 GMT  
		Size: 200.2 MB (200221618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:304e63e340214c7b274804a791fe847f10955783b6d5fed5e0d3e04afbaf64f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013d3b4f526af46a86bc8dc3c31b93a30c60249c9d0ee012ea9dddb2f3066e0f`

```dockerfile
```

-	Layers:
	-	`sha256:502c952ddb1183ed349b6e2aab646d43d288ffdac0b00e2684f27743c3caff19`  
		Last Modified: Wed, 11 Jun 2025 05:53:24 GMT  
		Size: 19.8 KB (19805 bytes)  
		MIME: application/vnd.in-toto+json
