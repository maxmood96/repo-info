## `dart:beta`

```console
$ docker pull dart@sha256:5526a543c34795cc013543f50b3e51a0bd8ec390bd03ad303d86ae12a5641289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:99d0abfe18a24ba6bfbaaff4512a8a2daaefa93dbc599e07e86d11827e4517ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 MB (322092593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c57d8f02b31347cca68f3414a00b27ad26cc9c12b5cf071d88cc5958f1bea6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:57:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:57:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 24 Apr 2024 07:57:51 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 24 Apr 2024 07:57:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 07:57:51 GMT
WORKDIR /root
# Wed, 24 Apr 2024 07:58:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=7c4652d0d1fe5f375d6d810e98dccaeda02d8dd9251babca4c53b7ec4c20a697;             SDK_ARCH="x64";;         armhf)             DART_SHA256=21d47dbdd97708adca357e780741c216bfeb7a4fcbe158e6cead99ba3c75f002;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e6bf4b25beb84aac39b6a472888230133c0324dd0dc4cf261176f8995fde6e0e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.4.0-282.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b486fdbe787723d2aa2760ebde6d9ffe73b2c4ba1d52377c5025d829da8d3e5`  
		Last Modified: Wed, 24 Apr 2024 07:58:47 GMT  
		Size: 54.7 MB (54657618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f2ab1db801be3cdebed116548f1c70e0574a55ce2f68049a8683719f80d40e`  
		Last Modified: Wed, 24 Apr 2024 07:58:39 GMT  
		Size: 1.8 MB (1800898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba81c5042d7107aafc483d20c65cd9c78f6b464ebca80c7974ea12ce57aad848`  
		Last Modified: Wed, 24 Apr 2024 08:00:01 GMT  
		Size: 236.5 MB (236483598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:29d8e0574337fc57660b3b6da0664edf1a1c3446cd1db79a270587617c1de70d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208855896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59bc200bdfb32ce7305ffbc4a63d1e6864b55939f94ff9a584f83c2b06c9a8ae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:05 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Wed, 24 Apr 2024 04:07:06 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:31:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:31:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 24 Apr 2024 04:31:54 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 24 Apr 2024 04:31:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 04:31:55 GMT
WORKDIR /root
# Wed, 24 Apr 2024 04:32:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=7c4652d0d1fe5f375d6d810e98dccaeda02d8dd9251babca4c53b7ec4c20a697;             SDK_ARCH="x64";;         armhf)             DART_SHA256=21d47dbdd97708adca357e780741c216bfeb7a4fcbe158e6cead99ba3c75f002;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e6bf4b25beb84aac39b6a472888230133c0324dd0dc4cf261176f8995fde6e0e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.4.0-282.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5e4769ba98641a6e96c662408d78dd11fff3529b2743d17a0c8ae4831f32b1`  
		Last Modified: Wed, 24 Apr 2024 04:32:46 GMT  
		Size: 49.1 MB (49137553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bf7f74e45cd9946dc92c8454914167b20c06ed01eaf7a15a6c842acf3df086`  
		Last Modified: Wed, 24 Apr 2024 04:32:39 GMT  
		Size: 1.2 MB (1227574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ba8ab266652461eadb6cb75bad0d71f1263107315240f9f02a6c0bc753758d`  
		Last Modified: Wed, 24 Apr 2024 04:33:41 GMT  
		Size: 133.8 MB (133750327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:2343293fd7f0bd73b5dc0b92ed250277bb592b058ad5dbef4cea9444a747baa0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.7 MB (320739583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fab8bdd2e3f9a2f4782fde6c154badccf1bc75f8e5851baf3944d7d161ae9a0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:10:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:10:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 10 Apr 2024 05:10:42 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 10 Apr 2024 05:10:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 05:10:42 GMT
WORKDIR /root
# Thu, 18 Apr 2024 18:03:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=7c4652d0d1fe5f375d6d810e98dccaeda02d8dd9251babca4c53b7ec4c20a697;             SDK_ARCH="x64";;         armhf)             DART_SHA256=21d47dbdd97708adca357e780741c216bfeb7a4fcbe158e6cead99ba3c75f002;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e6bf4b25beb84aac39b6a472888230133c0324dd0dc4cf261176f8995fde6e0e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.4.0-282.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911af322132dafaa481fc7abdb6102f8ca1a90809c49105ea9932927d01dd2a0`  
		Last Modified: Wed, 10 Apr 2024 05:11:51 GMT  
		Size: 54.3 MB (54322806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c11a32dfaef706716ccfd5326eaa26ff711af44ed507b45c9089db9bab3386db`  
		Last Modified: Wed, 10 Apr 2024 05:11:46 GMT  
		Size: 1.5 MB (1493768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f612ffa5cbbb053a290620c2b84673f3e1e9773295d1dd17cde2cd3efe339f2`  
		Last Modified: Thu, 18 Apr 2024 18:05:10 GMT  
		Size: 235.8 MB (235760852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
