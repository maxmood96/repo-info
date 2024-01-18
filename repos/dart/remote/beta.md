## `dart:beta`

```console
$ docker pull dart@sha256:35a564dea0481148ba3dc19d664f92d6d460d6a494e209fd903b0ca6772bdbac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:211367b234f8fcabb4528418cecae2339116d049025fcc050a2c53e83261c4b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314046377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02696d8531a72724ec6d3bc896503c95303ee4bac329fa2247947cae11f4af61`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:28:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:28:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 05:28:12 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 05:28:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:28:12 GMT
WORKDIR /root
# Thu, 18 Jan 2024 18:56:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a7ed5168acabce7cfb292de210d5fedb33a481548470a6e8142b20946ca81cfb;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de28b2ab3d772026ee92d2911c0c476c147341d67a0d1f33a82ba9ba858a960e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e9516c29f1261dd985685a0d1e68ec85c531795e6aed6d7da72604a9a978e9b9;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.3.0-279.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc143d38f00257638c6f6afde350c5dd5e5c82b5f7f1dd755ff76ef726f94c3e`  
		Last Modified: Thu, 11 Jan 2024 05:29:10 GMT  
		Size: 54.7 MB (54650943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffd9b595c430cc5ffcfec691b3fccdaedd13ec56f1222af7d606a3892410d10`  
		Last Modified: Thu, 11 Jan 2024 05:29:06 GMT  
		Size: 1.8 MB (1800649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d9ba3faa32de9687a547526617d1a9a9fd18cc3c955e2995fa64d3029a86e5`  
		Last Modified: Thu, 18 Jan 2024 18:57:53 GMT  
		Size: 228.5 MB (228468864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:8ffe3d856e6ee33931693f5d18df53047cc0bc20de41f1f9ec25406138d11b34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.8 MB (202828664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d435565edccf3fa8c3b163b3f557193999079cb0a6cab0862a7498df514803`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 19:50:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:50:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 19:50:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 19:50:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 19:50:35 GMT
WORKDIR /root
# Thu, 11 Jan 2024 19:51:19 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=24fee21a8e378050b0b0611602f674059d5a93bb09a560539857e384f1b83056;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2cccf79d89105294c46881f0f7d7e1f574d6cb2d8a12de7d0a04311dcde6acb2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f86de4ab4f99a2dbdc6a0809acaae40a280fa3cbac340bbdf910cf7f0085dcbb;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.3.0-174.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98606fa9f3adbeb573a3b9cd538f16226ba753a62994751b3f9308ee7a3c3985`  
		Last Modified: Thu, 11 Jan 2024 19:51:49 GMT  
		Size: 49.1 MB (49133316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0775197d864e5d5a2f4f33d2f5b8604f3399d6443fe0413d94896ed6b081ec`  
		Last Modified: Thu, 11 Jan 2024 19:51:38 GMT  
		Size: 1.2 MB (1227213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddb42c84b964f5b8d632d49b20f29c8af0e74f876d2c3bb0811b613ac147b2d`  
		Last Modified: Thu, 11 Jan 2024 19:52:53 GMT  
		Size: 127.8 MB (127750009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:889bd9a67f8bf0d21ba796d00e6512fb01ffbdd31655ecc3da7131cf698d2419
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312694175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f64645b69ae1d862850eee01d45e7ce233936d89c727541c8463ff182a75bc8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:44 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Thu, 11 Jan 2024 02:40:45 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:09:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:09:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 06:09:23 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 06:09:23 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:09:23 GMT
WORKDIR /root
# Thu, 18 Jan 2024 18:54:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a7ed5168acabce7cfb292de210d5fedb33a481548470a6e8142b20946ca81cfb;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de28b2ab3d772026ee92d2911c0c476c147341d67a0d1f33a82ba9ba858a960e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e9516c29f1261dd985685a0d1e68ec85c531795e6aed6d7da72604a9a978e9b9;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.3.0-279.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0552868b6e7201868baa0a0c3e2bbfc0b8ff428ce113640f0618975355e701ff`  
		Last Modified: Thu, 11 Jan 2024 06:10:23 GMT  
		Size: 54.3 MB (54320572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be68e932669157661281daca517662d68384289b53e2db9ed1d21267100a382`  
		Last Modified: Thu, 11 Jan 2024 06:10:18 GMT  
		Size: 1.5 MB (1493536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc1fbd0e32063bad84e913983edeae8a51c706d263befa933112239755445da`  
		Last Modified: Thu, 18 Jan 2024 18:56:28 GMT  
		Size: 227.7 MB (227722732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
