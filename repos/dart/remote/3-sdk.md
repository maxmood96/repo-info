## `dart:3-sdk`

```console
$ docker pull dart@sha256:1daa53cdfd134254c7a40958ff238a3a1348d4ad999544b292e43602bd19379f
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
$ docker pull dart@sha256:7fc357d38c580bcfc34eca9e2a06f2ad281e65225c83caf4aa4f9b690bfd39db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304959250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d47c7a181c02c24eafa605b35f1eb182fe66530cc337c313333e744d26048f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8863d077341b75b5d7f450b7cf236572e41553c9c8a00d16fea4b689bbf397`  
		Last Modified: Wed, 12 Feb 2025 18:31:20 GMT  
		Size: 54.9 MB (54906479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6634beef04ea247e5b82bf8f3a55a95bd82134f7b870d1e94c76af605c6030c8`  
		Last Modified: Wed, 12 Feb 2025 18:31:20 GMT  
		Size: 1.8 MB (1796912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d89a1056992245a075937329419a9ecb37300c0c953051f808bcb0ae623a0d`  
		Last Modified: Wed, 12 Feb 2025 18:31:23 GMT  
		Size: 220.0 MB (220043524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:f8298b31be34d039191a1527ddc1c54596a122043fef906ebe102c0ada4c4150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0650f73d6cdf5ee46fc89967b194d257972d03c772213bf8763b1691a05dd925`

```dockerfile
```

-	Layers:
	-	`sha256:438bf545029f71e6751a95c5620c5f2d7745a6ecd3d56fc600603dd85e4e9ab3`  
		Last Modified: Wed, 12 Feb 2025 18:31:20 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:a6a5dc0260acb7755a29d1bddbeb77efecca0e2867a394d9e9ef2100d4ced803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226295222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea954d4a886089a124ff83da6f2cf091ed2efbb8a941e4fa11736fb0b17f4b68`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b452fdef5dac9c8f8fe51d8f4387c17e0bf52d4e842afdf1faafca8550c46bf`  
		Last Modified: Wed, 12 Feb 2025 18:37:51 GMT  
		Size: 49.6 MB (49561606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6baa8589f92b768e7f9d2ad72e20d17de70780ed721a90c0224d66c3b342be75`  
		Last Modified: Wed, 12 Feb 2025 18:37:49 GMT  
		Size: 1.2 MB (1221677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c6877a3ba763df6cf5d989c8634dfe93112f1fcc6e9a677bdf30614bdf46d6`  
		Last Modified: Wed, 12 Feb 2025 18:37:53 GMT  
		Size: 151.6 MB (151597371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:830cac7a383008478cfd07386e23d6f26561eaa6624e2696402937564ea1e982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440338683c877b03487e63fe4c0de94d7b081e81356e40d1bad1369c76768cf8`

```dockerfile
```

-	Layers:
	-	`sha256:6998fad4826e8e73cae23710077b9ccf19963390bad92cd9c76f2dbf34ec8497`  
		Last Modified: Wed, 12 Feb 2025 18:37:48 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3eb11543afe931665e7c05b7a4c575bb7f9e381e12a9eb631b36f38427026ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303817925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cffe03d061e88fab4ae9c44614ecb0d16e0623eb49b97db96ccf531b3379e23`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Feb 2025 08:49:18 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Feb 2025 08:49:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Feb 2025 08:49:18 GMT
WORKDIR /root
# Wed, 12 Feb 2025 08:49:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=367b5a6f1364a1697dc597775e5cd7333c332363902683a0970158cbb978b80d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=03842c2037f99450a1433f5dab9dc1820686eadf92f517929d0306cbbe92ecd2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=7c849abc0d06a130d26d71490d5f2b4b2fe1ca477b1a9cee6b6d870e6f9d626f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b82a1454208f1a1f6748f7f37c3a77702ba1824759702373423939a1800a632`  
		Last Modified: Wed, 12 Feb 2025 18:36:44 GMT  
		Size: 54.7 MB (54678762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd3240157b9d992362b3857e7d1ea5c71920efe6c800ac83adbef4415df3dcf`  
		Last Modified: Wed, 12 Feb 2025 18:36:43 GMT  
		Size: 1.5 MB (1488030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad74ed0fbf3d9b837a721284f3926c683f00b9978969aa882f3c762686b1ca66`  
		Last Modified: Wed, 12 Feb 2025 18:36:48 GMT  
		Size: 219.6 MB (219610220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b9a9edc95f40664cfbc3fe9e5fe2166525019b882be2be8354aeb217abc09c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6093326d1775e44a2cd0a599a0853a750c4bc45d1f91a55808e16b5c6c4a6f1`

```dockerfile
```

-	Layers:
	-	`sha256:a56afa6edb6ae77d867153e8a968a75b88b49bd80da34d6bb1ea8a61edaa046b`  
		Last Modified: Wed, 12 Feb 2025 18:36:42 GMT  
		Size: 19.8 KB (19805 bytes)  
		MIME: application/vnd.in-toto+json
