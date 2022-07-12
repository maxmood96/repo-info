## `dart:stable-sdk`

```console
$ docker pull dart@sha256:d3f2f27245c51c6351fc2dfa4792e9ab34c6fff680a7d76121aee361137b7029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:7061b1fb27726f585ff458ed53758a02245ff73d6d9dbc7b034cbb92140ec0df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.8 MB (275797927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5cd1d06eb0a4c4aa8cf018a65e3c95b2bfaa28d210945e73bd53862a4ffa978`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:59:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:59:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 12 Jul 2022 02:59:02 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 12 Jul 2022 02:59:02 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 02:59:02 GMT
WORKDIR /root
# Tue, 12 Jul 2022 02:59:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0052467a23ec8d46523be0f29263881444e0da3228860eb6b69de0859aca2459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=00e855429cd7345a56235a7b216967d23c22d0c1a0417249c4323b1cbfe9af62;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0482ba914c7e9befc67d1ff0057bfcae354d6cfeb0d4716f1ff44623089a2688;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.17.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f917959e81624996e9066796ed3b4d6e571cbc880050ada2576bb98642763bb`  
		Last Modified: Tue, 12 Jul 2022 03:00:00 GMT  
		Size: 45.1 MB (45073315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71203ed23ff0af6379c663fda23420d4da991909927621bc682b67d48328d642`  
		Last Modified: Tue, 12 Jul 2022 02:59:53 GMT  
		Size: 2.1 MB (2139541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e331ac2bb3468d94a7ce3b2237db4a9ef35539752fe7e1e60a4cf62e392ff845`  
		Last Modified: Tue, 12 Jul 2022 03:00:22 GMT  
		Size: 197.2 MB (197218461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:d6828fadccaceccc8072eac73568ce163ac21126316f3282b1154709058446ec
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.1 MB (184059360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f8268d479dadb534ab5c992fd0faa90367eff3026b97dd1d5d5944c6e00898`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:59:54 GMT
ADD file:ae890621b36ff6e27364bb7316b5bd4319a820ddf7e65565c6201eb11d70fde9 in / 
# Tue, 12 Jul 2022 00:59:55 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 04:00:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 04:00:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 12 Jul 2022 04:00:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 12 Jul 2022 04:00:59 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 04:00:59 GMT
WORKDIR /root
# Tue, 12 Jul 2022 04:01:19 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0052467a23ec8d46523be0f29263881444e0da3228860eb6b69de0859aca2459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=00e855429cd7345a56235a7b216967d23c22d0c1a0417249c4323b1cbfe9af62;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0482ba914c7e9befc67d1ff0057bfcae354d6cfeb0d4716f1ff44623089a2688;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.17.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:314cda9d0ef2282082d2bd0efd7659e0d9edb3ceae8e7919d990bcf95cbb3d2b`  
		Last Modified: Tue, 12 Jul 2022 01:12:37 GMT  
		Size: 26.6 MB (26560559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4316fd66656dd89ade0257dac476c6229bb11452333cb88904df00760175d4`  
		Last Modified: Tue, 12 Jul 2022 04:03:48 GMT  
		Size: 41.0 MB (40966440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de87ab189edecdb2c70e7ebd1274844a743ed886eace795c9d9eeef8a499e64`  
		Last Modified: Tue, 12 Jul 2022 04:03:24 GMT  
		Size: 1.3 MB (1288082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ca16399f4184877ecbc3567a5c1144991fcdf3c3d2824971c2b8c55363cd5f`  
		Last Modified: Tue, 12 Jul 2022 04:04:38 GMT  
		Size: 115.2 MB (115244279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:1cf988fa236f63c4fac926118eafadf43ba12418d47047b99fea30d431d5f42b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193347795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1961915744ae24c7f368107c647c4240ca0c395d4c406d906dd07bd3393627c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:34 GMT
ADD file:f3a33075f4c3324c6a634ef37a1965ddd5606b4449c0f5909ce18eeb8268b612 in / 
# Tue, 12 Jul 2022 00:40:35 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:50:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:50:26 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 12 Jul 2022 02:50:26 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 12 Jul 2022 02:50:27 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 02:50:28 GMT
WORKDIR /root
# Tue, 12 Jul 2022 02:50:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0052467a23ec8d46523be0f29263881444e0da3228860eb6b69de0859aca2459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=00e855429cd7345a56235a7b216967d23c22d0c1a0417249c4323b1cbfe9af62;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0482ba914c7e9befc67d1ff0057bfcae354d6cfeb0d4716f1ff44623089a2688;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.17.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:60197a4c18d4b386d371cf39d01c48e98c357bba06da0b070a3c1f75006fd838`  
		Last Modified: Tue, 12 Jul 2022 00:46:13 GMT  
		Size: 30.1 MB (30054226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e246275131a2c58b895f382305d66ca2a62c8a433f275f1af8487179ec55d8`  
		Last Modified: Tue, 12 Jul 2022 02:51:50 GMT  
		Size: 45.0 MB (44993733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21622692fc0cf8e1b2d476c3dd08928da6df9f71f634746ca0362125b8b58dd`  
		Last Modified: Tue, 12 Jul 2022 02:51:43 GMT  
		Size: 1.6 MB (1556731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c5450489cf80a958668668700323ef2e5fc0e061f76d701f697427076aa78d`  
		Last Modified: Tue, 12 Jul 2022 02:52:03 GMT  
		Size: 116.7 MB (116743105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
