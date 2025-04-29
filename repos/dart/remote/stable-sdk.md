## `dart:stable-sdk`

```console
$ docker pull dart@sha256:fd78e3d32390016c37795d4b9131bcec0f7db7e7d90d4eb0fbcfdcc766e1cdee
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
$ docker pull dart@sha256:cb058b6e238fb47563bfc0f5bba26213fe470cf1d409c88064c725fe300bc1d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305383878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53275b4e087fbca865a678bb95fa00863d681e277e89ef98d7fa721913d6e9ad`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Apr 2025 07:27:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c9c6249818b708b31f06e7177c831e81e55d134630a3d3ea8a644ab2d4236f`  
		Last Modified: Mon, 28 Apr 2025 21:56:05 GMT  
		Size: 54.9 MB (54906293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6359fcff80b4250b79bdbfed370d19995ab184a08a8409a447ee8d3ec1bd6e56`  
		Last Modified: Mon, 28 Apr 2025 21:56:04 GMT  
		Size: 1.8 MB (1785447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7304989f6c7cae3181c81cc46ccd500559c54b83cb908f853d8b039f16ccb805`  
		Last Modified: Mon, 28 Apr 2025 21:56:10 GMT  
		Size: 220.5 MB (220464464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:dba93c51590f6a7712151e670a368b01eb4414f364ce8167cf10dc0e4d8df977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7355d27488c9810c7c987d733704ee0dcad94cf92273f620db247581c6a3cf`

```dockerfile
```

-	Layers:
	-	`sha256:5eff83b85748339a47ff72104d97d79aa9e8856eb882b20d3c7f0dd45b71dc18`  
		Last Modified: Mon, 28 Apr 2025 21:56:04 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:fa5f01498124bfc93a26439dcf18337f8c39eabe33c81a65754c687e0b3042fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228435602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ed14046d61d7c42e7587c103375c0f48ecf86dd214519144ea99799fae8107`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1330b2381da106ae28676390c114d27603e3d27780aa9cf44a256c87c17d3f73`  
		Last Modified: Thu, 17 Apr 2025 18:50:34 GMT  
		Size: 51.7 MB (51680929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa2189d0ec2c0aa10e7cd73369cd1a292f801f44dae53b2dca0bfc1de42f32b`  
		Last Modified: Thu, 17 Apr 2025 18:50:33 GMT  
		Size: 1.2 MB (1221946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7f0fbeee15e07c6f2dbd37cc4288a12b1ffeec74ae9f0db7559cc82f3cb070`  
		Last Modified: Thu, 17 Apr 2025 18:50:37 GMT  
		Size: 151.6 MB (151594828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c1705a576066009b8acd8340f301e35c3586a5e494d4c97a95f4210fa520dd98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed8a1f7a28dd3dc02b86835f8a5e30ec682670bb62ce8239c953083d86e9410`

```dockerfile
```

-	Layers:
	-	`sha256:80b02523c75524fd9b92278f18632f57254f9409b1c39c6b0b4f490e0b5774e9`  
		Last Modified: Thu, 17 Apr 2025 18:50:32 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:31e53ff6933550ee2e292201648ccdddb654bf2e65c756c739ded1dc2ac7ea50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303860096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c36e8f0daac774d32ab28160c3ca4466dd6ed1e514ae92d9a32a61df4828bbf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Apr 2025 07:27:52 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4551d193349534fd6fc42db43a320398afa226684e8eb77e030f7bb9e557b8e`  
		Last Modified: Tue, 29 Apr 2025 01:53:15 GMT  
		Size: 54.7 MB (54679866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503cf2ea4264ce253bcdd93daa00d352bea16c344fc51a0fc05441edd023c757`  
		Last Modified: Tue, 29 Apr 2025 01:53:13 GMT  
		Size: 1.5 MB (1488223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811a6cd6820b64fc5eeac1af4ca99be62718928b76595f8c3c5d6fbf901b353c`  
		Last Modified: Tue, 29 Apr 2025 01:53:18 GMT  
		Size: 219.6 MB (219625353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:706856c660ae843f687c4d9722e1c5a29ad507dcab9d014d7195f0cdc9760639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c74029cc5c2911566e21feafa29a525812bc42fa47e52dbb09a2f998c0f4162`

```dockerfile
```

-	Layers:
	-	`sha256:7e8b766dc6a937053b4eb7feac5f04a87d3004149581f2434500b78331af900e`  
		Last Modified: Tue, 29 Apr 2025 01:53:13 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json
