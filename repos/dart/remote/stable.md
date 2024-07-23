## `dart:stable`

```console
$ docker pull dart@sha256:31fbf1dd6b7d16df608e422b69518fa6c34baed1df7b0d1315d3e12ea01dd7d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:9a63202f1c64c57b8e75ce41d98b1891f97bdf82daa2fc90dd1f1b110a376a45
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 MB (322117937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd88d5df076f1bee11a37fca298f199d81f35b400d89f93dba1a090b0921029`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:15 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Tue, 23 Jul 2024 05:24:16 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:18:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:18:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 23 Jul 2024 06:18:47 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 23 Jul 2024 06:18:47 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 06:18:48 GMT
WORKDIR /root
# Tue, 23 Jul 2024 06:19:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ca7630c6fe5629e043e648c701e2f1d935d28f18ef688edfb0da76f11e3eed`  
		Last Modified: Tue, 23 Jul 2024 06:19:42 GMT  
		Size: 54.7 MB (54657285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40457f989c7144f0efee686bd50a04ae1518eef25314f1d7adc46e8af69f1256`  
		Last Modified: Tue, 23 Jul 2024 06:19:34 GMT  
		Size: 1.8 MB (1800894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91dd2137f082520acab8d81080a4d2cf73823450cbb56b7f1956e895c598a7d`  
		Last Modified: Tue, 23 Jul 2024 06:20:04 GMT  
		Size: 236.5 MB (236533471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d911a0965d27c8147330176cde3fac41e459bb2d1e62df13fa92da9067636b7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208860086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e5424e0795bd35b810833d2c756d92ce339a5e2f188ce7d8829cd6da97e15a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:06 GMT
ADD file:b3438b93a141bfac397342418c34c4fe554bd257eeee378da353577c3d2206ca in / 
# Tue, 23 Jul 2024 03:03:07 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:21:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 04:21:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 23 Jul 2024 04:21:45 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 23 Jul 2024 04:21:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 04:21:46 GMT
WORKDIR /root
# Tue, 23 Jul 2024 04:22:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:ec16b40bfa260bcfd3b351a12bda1032683bb7db1fc4a9630b03194691569e14`  
		Last Modified: Tue, 23 Jul 2024 03:06:55 GMT  
		Size: 24.7 MB (24718200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db529479e59d671ef4a2396332d685fcec9f9c360b2caeb182958f027dcdc728`  
		Last Modified: Tue, 23 Jul 2024 04:23:00 GMT  
		Size: 49.1 MB (49133331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8918e5ad0a2e11b87a9946f1dfa9f9423c499d8f4d7e7572cdf8614c4dee159`  
		Last Modified: Tue, 23 Jul 2024 04:22:47 GMT  
		Size: 1.2 MB (1227543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4231d69097aa5c078eabfe63f37350b8f909952d964c7037565f361c1d597bb7`  
		Last Modified: Tue, 23 Jul 2024 04:23:15 GMT  
		Size: 133.8 MB (133781012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:6ab5b7f0e4b81009fcfa75cdef13fe5979989032216aa9d31962bcb6d06519fd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.8 MB (320809736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee3f1bd7bcc89a06e85c21730a6234a7588ea4540b2dccb95397163fa2b37be`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:51 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Tue, 23 Jul 2024 04:17:52 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 05:06:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 05:06:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 23 Jul 2024 05:06:37 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 23 Jul 2024 05:06:37 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 05:06:37 GMT
WORKDIR /root
# Tue, 23 Jul 2024 05:06:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9dd554d5b30e57401d3f576465511cda0511fb4aca0c8537156b555e48d1cc`  
		Last Modified: Tue, 23 Jul 2024 05:07:43 GMT  
		Size: 54.3 MB (54319001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b887b17e978d121abdc33180e57178e681539227b2fd918a2469830b060201`  
		Last Modified: Tue, 23 Jul 2024 05:07:38 GMT  
		Size: 1.5 MB (1494267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9e9a9170bcc8c591d52712ebb7b4c85acc1ff60bd370ae646f3829bdf50ed4`  
		Last Modified: Tue, 23 Jul 2024 05:08:02 GMT  
		Size: 235.8 MB (235839897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
