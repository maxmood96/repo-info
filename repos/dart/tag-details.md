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

**does not exist** (yet?)

## `dart:3.9.0-196.1.beta-sdk`

**does not exist** (yet?)

## `dart:beta`

```console
$ docker pull dart@sha256:c5c200f823a330570e2c7f7ac0ca8c889b70f560b6ab8eb4f9772b6ac5b5a0eb
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
$ docker pull dart@sha256:5d888be9846c532344d05b6f13839927d730605745c04a0af0ac0e554c988527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299689541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c1d1c36b1c2a4de2174a953a69a7ab4d7baf19195150bb9564e86117b5b075`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f33d48dfc86a27225aa51bc551e06d5e9b887629734d5092a1ebbd8b335b1d8`  
		Last Modified: Tue, 10 Jun 2025 23:38:16 GMT  
		Size: 54.9 MB (54910720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6853985df31105cf89cf292948b277ff2816ae7a60d3e5a32587d721ba05fe80`  
		Last Modified: Tue, 10 Jun 2025 23:38:13 GMT  
		Size: 1.8 MB (1785455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6993d884f519802900d62300fd633fd5af3db6049f2a4b4a7eecc42512f44b29`  
		Last Modified: Wed, 11 Jun 2025 02:54:16 GMT  
		Size: 214.8 MB (214763205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:dbdfeab728878108a88ff7a8875b5c4a3c300a27b2da644f04b3fec04bce1815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733687fb7d40292ab6acd024d1ee160e7dbd5d4fe47aeff125d8768b488ebd04`

```dockerfile
```

-	Layers:
	-	`sha256:e584035d72ff39d8d3ecc9e3bd065f2f5724da8f7921c3f1ca4156208d5d81c1`  
		Last Modified: Wed, 11 Jun 2025 02:53:29 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:57dac6b76a8ab45e4619e2bf0b67fa5c874b855631b48f6ad1b133b0190dd0a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223856833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0861f7ecc71b50919246de315ae6433c03c25a38fb9cc08ebd978d8c869f896b`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
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
	-	`sha256:a06987574ea943cdf616c540fd08c685f14f28a50afb74259407bd9d6f1aaf54`  
		Last Modified: Wed, 11 Jun 2025 05:53:55 GMT  
		Size: 149.1 MB (149141422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:b1e71cd7e6837af31b5ebb3af95fdc371ce229980f632e5e1423c73b29620ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bb256871b9747a292a66f4de6e8104fa7267daaad47abd63111918837aaa5f`

```dockerfile
```

-	Layers:
	-	`sha256:fce8eb28ec485ff1381f34d1afd0715e52e7eaba30889968fdd4c2dc1ab20068`  
		Last Modified: Wed, 11 Jun 2025 05:53:34 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:6db336e6c7de59ede6b1e0b08740dc0d7f0ae1b5bd9bdbd05c82902e7e8d344d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298396879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc881bb6a2439a3726a8b078ddd5cec0bb8af877d1f2dffc8ae7f39c08a4a83`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
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
	-	`sha256:cc8dca186af51e99f3db9def1d8d5cffaccfba3fa655d30053618fc2f92e519b`  
		Last Modified: Wed, 11 Jun 2025 05:53:49 GMT  
		Size: 214.1 MB (214148172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:c47483c8b3e629f4d745a597c1adc86ada6f4e645e6ca289e8da606ca1d678da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f952aa626abde6dd38d31b673b212974ed1f54968e4014ffda56d7ed9beb4d92`

```dockerfile
```

-	Layers:
	-	`sha256:c8664f9bf4de30c10bc419c700cf41148b8f8215226462d1a5f628b4cc43ff15`  
		Last Modified: Wed, 11 Jun 2025 05:53:38 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:c5c200f823a330570e2c7f7ac0ca8c889b70f560b6ab8eb4f9772b6ac5b5a0eb
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
$ docker pull dart@sha256:5d888be9846c532344d05b6f13839927d730605745c04a0af0ac0e554c988527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299689541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c1d1c36b1c2a4de2174a953a69a7ab4d7baf19195150bb9564e86117b5b075`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f33d48dfc86a27225aa51bc551e06d5e9b887629734d5092a1ebbd8b335b1d8`  
		Last Modified: Tue, 10 Jun 2025 23:38:16 GMT  
		Size: 54.9 MB (54910720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6853985df31105cf89cf292948b277ff2816ae7a60d3e5a32587d721ba05fe80`  
		Last Modified: Tue, 10 Jun 2025 23:38:13 GMT  
		Size: 1.8 MB (1785455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6993d884f519802900d62300fd633fd5af3db6049f2a4b4a7eecc42512f44b29`  
		Last Modified: Wed, 11 Jun 2025 02:54:16 GMT  
		Size: 214.8 MB (214763205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:dbdfeab728878108a88ff7a8875b5c4a3c300a27b2da644f04b3fec04bce1815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733687fb7d40292ab6acd024d1ee160e7dbd5d4fe47aeff125d8768b488ebd04`

```dockerfile
```

-	Layers:
	-	`sha256:e584035d72ff39d8d3ecc9e3bd065f2f5724da8f7921c3f1ca4156208d5d81c1`  
		Last Modified: Wed, 11 Jun 2025 02:53:29 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:57dac6b76a8ab45e4619e2bf0b67fa5c874b855631b48f6ad1b133b0190dd0a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223856833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0861f7ecc71b50919246de315ae6433c03c25a38fb9cc08ebd978d8c869f896b`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
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
	-	`sha256:a06987574ea943cdf616c540fd08c685f14f28a50afb74259407bd9d6f1aaf54`  
		Last Modified: Wed, 11 Jun 2025 05:53:55 GMT  
		Size: 149.1 MB (149141422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b1e71cd7e6837af31b5ebb3af95fdc371ce229980f632e5e1423c73b29620ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bb256871b9747a292a66f4de6e8104fa7267daaad47abd63111918837aaa5f`

```dockerfile
```

-	Layers:
	-	`sha256:fce8eb28ec485ff1381f34d1afd0715e52e7eaba30889968fdd4c2dc1ab20068`  
		Last Modified: Wed, 11 Jun 2025 05:53:34 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:6db336e6c7de59ede6b1e0b08740dc0d7f0ae1b5bd9bdbd05c82902e7e8d344d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298396879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc881bb6a2439a3726a8b078ddd5cec0bb8af877d1f2dffc8ae7f39c08a4a83`
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
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
	-	`sha256:cc8dca186af51e99f3db9def1d8d5cffaccfba3fa655d30053618fc2f92e519b`  
		Last Modified: Wed, 11 Jun 2025 05:53:49 GMT  
		Size: 214.1 MB (214148172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c47483c8b3e629f4d745a597c1adc86ada6f4e645e6ca289e8da606ca1d678da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f952aa626abde6dd38d31b673b212974ed1f54968e4014ffda56d7ed9beb4d92`

```dockerfile
```

-	Layers:
	-	`sha256:c8664f9bf4de30c10bc419c700cf41148b8f8215226462d1a5f628b4cc43ff15`  
		Last Modified: Wed, 11 Jun 2025 05:53:38 GMT  
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
