## `dart:stable`

```console
$ docker pull dart@sha256:47385e356b6de64cc5f310486eff521459a2db5488d7f85a846e829b7b8a7e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:91b3e8f1c5d690cb70af18c50cc6192363b58cd17404b231d0a4367813752fd5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.9 MB (302918227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7e15819c5c5197291e60649f9c1418922cd6b22e33bfe721413cb22389975f`
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
# Tue, 06 Aug 2024 20:19:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=011a1dd6ff4e0bb4a168f7b4e13063514fbc255dc52d1ad660bf5a28773e9773;             SDK_ARCH="x64";;         armhf)             DART_SHA256=dec85f8439ae55f30cc29ad80b6486acd20c97b25dcaa1b3d05caab36c980323;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ee2cbcc36a190a883254ddc28ef772c15735022bfc5cfc11a56dbaebd5353903;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:2336b199e631359dc15c606ff5904aa3da621783ffbb4e372fcc56bc00e9f275`  
		Last Modified: Tue, 06 Aug 2024 20:20:23 GMT  
		Size: 217.3 MB (217333761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:e4ebcb920a838c557697a8f45de9861ba8cde6714d8bb956c53dfe91250eea65
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.1 MB (203148285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a465a6cc767fcd8da9790ab67acac83866ebb9e77ce3784410909d82d55e51b3`
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
# Tue, 06 Aug 2024 19:58:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=011a1dd6ff4e0bb4a168f7b4e13063514fbc255dc52d1ad660bf5a28773e9773;             SDK_ARCH="x64";;         armhf)             DART_SHA256=dec85f8439ae55f30cc29ad80b6486acd20c97b25dcaa1b3d05caab36c980323;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ee2cbcc36a190a883254ddc28ef772c15735022bfc5cfc11a56dbaebd5353903;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:9c8eb9cccefdc99a29085d387b823b3c8014310c20ed5e2c207df55ea93bf5ce`  
		Last Modified: Tue, 06 Aug 2024 19:59:29 GMT  
		Size: 128.1 MB (128069211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4ab0d2280677bb5110b7c7da69fc6ce068cb084a1255ed5dd05653cadb82d775
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301465719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48070f5777f92e41c4148d0a69df855d0a166fab184c641d848f9e1859ce1550`
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
# Tue, 06 Aug 2024 19:39:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=011a1dd6ff4e0bb4a168f7b4e13063514fbc255dc52d1ad660bf5a28773e9773;             SDK_ARCH="x64";;         armhf)             DART_SHA256=dec85f8439ae55f30cc29ad80b6486acd20c97b25dcaa1b3d05caab36c980323;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ee2cbcc36a190a883254ddc28ef772c15735022bfc5cfc11a56dbaebd5353903;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:6570a285ddef120dc3ab9605fa372eb7c36c45aa004588df998365d7f0e94a2f`  
		Last Modified: Tue, 06 Aug 2024 19:40:22 GMT  
		Size: 216.5 MB (216495880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
