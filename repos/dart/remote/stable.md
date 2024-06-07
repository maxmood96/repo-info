## `dart:stable`

```console
$ docker pull dart@sha256:57ba682e66bd8a1ece4292f15419e5be53803512811635c664399a6ee9aaa894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:cc2b663c8f3e770f96294df05c013a047aa91195bcd5b89da2b66a4e414516f7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 MB (322135419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f938b023d764552a83b5eacd9c454c604e947a421c7afa89fbb90d0cb0d239`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Thu, 30 May 2024 18:45:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 30 May 2024 18:46:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 30 May 2024 18:46:01 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 May 2024 18:46:01 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 18:46:01 GMT
WORKDIR /root
# Thu, 30 May 2024 18:46:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=43a60e3a15a52fd584b0eddd235f0afeffed50f6e15a56f4ad74d83ee8fb5943;             SDK_ARCH="x64";;         armhf)             DART_SHA256=11a6e8ee6f0f449fb1f1657cb35acea3f75234de02c735fd06fc61ccb6dfd1eb;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4e0ce122acc157d3177c0911c79ec25560d6465d8adc17a4de10d824aa14d0de;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50117cb7d037f93345bbf8ed600840ace867b7f93409890a34d94423c29fd339`  
		Last Modified: Thu, 30 May 2024 18:47:00 GMT  
		Size: 54.7 MB (54657787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcca7dab253880d57aa17dc7506179255988742d1c72038a572481be76f9085d`  
		Last Modified: Thu, 30 May 2024 18:46:52 GMT  
		Size: 1.8 MB (1800894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13bafcd8d255f91c1e3303e207c0f8f78e4fcf39f455d32636c2a66a6134523`  
		Last Modified: Thu, 30 May 2024 18:47:23 GMT  
		Size: 236.5 MB (236526327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:af28e7eca63e749e4c975ff3967a9294c1d844be5be745b876b9ad000021ab49
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208870915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f7e832631016d692844a64f15d3eb0bed3f91dc19483d986baa71bb1205a26`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Thu, 30 May 2024 19:12:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 30 May 2024 19:12:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 30 May 2024 19:13:00 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 May 2024 19:13:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 19:13:00 GMT
WORKDIR /root
# Thu, 30 May 2024 19:13:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=43a60e3a15a52fd584b0eddd235f0afeffed50f6e15a56f4ad74d83ee8fb5943;             SDK_ARCH="x64";;         armhf)             DART_SHA256=11a6e8ee6f0f449fb1f1657cb35acea3f75234de02c735fd06fc61ccb6dfd1eb;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4e0ce122acc157d3177c0911c79ec25560d6465d8adc17a4de10d824aa14d0de;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f465c681dbcf5016dfbb81617192cb52560d1d6538f79abfd8b3af8ba9f16bae`  
		Last Modified: Thu, 30 May 2024 19:13:53 GMT  
		Size: 49.1 MB (49137541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f3b0cc525220cb01782f1cb3bb2ea5d4a5fd5147e7034374e34a7dd2237422`  
		Last Modified: Thu, 30 May 2024 19:13:47 GMT  
		Size: 1.2 MB (1227577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae810e903a6b0aed1e5aa1c6d1befd53e132e139527dc3924d1e81eac064335`  
		Last Modified: Thu, 30 May 2024 19:14:06 GMT  
		Size: 133.8 MB (133765592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:cdcc454aa662145ae7b90ebaec0af935973ed5e507e5967fe0ef6b0c66962534
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320863271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb22132002fa2e98da83da97efcc0e762d3d8466daaaaba4ff14da99323f516`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Thu, 30 May 2024 18:53:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 30 May 2024 18:53:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 30 May 2024 18:53:14 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 May 2024 18:53:14 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 18:53:14 GMT
WORKDIR /root
# Fri, 07 Jun 2024 01:10:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6366ae94486d27a0d450c0d9bb35b181978f700c7a547e98ab50dbc8fb6ecca3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ffc16f542700371fa2ed1e2b18d72e804f67375f6f6dcf0c8dc0f014f16d70bc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c155e6d2f09a3d0fe04de4600040798ee253662017e46bb451787c62f19bd576;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e74d7932a78ab59a695b27e7239a32426ac9f446cc1c2ee48d39c375a8a8745`  
		Last Modified: Thu, 30 May 2024 18:54:22 GMT  
		Size: 54.3 MB (54326192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5826170ff72754adb19c8ff12c6b6c54cf83ec92fa7c0af6acaa10241cec030c`  
		Last Modified: Thu, 30 May 2024 18:54:17 GMT  
		Size: 1.5 MB (1494305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f59cb7985e34b07b18bda983e106d79169538565de12e91dfabf99afbf0907e`  
		Last Modified: Fri, 07 Jun 2024 01:11:27 GMT  
		Size: 235.9 MB (235863271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
