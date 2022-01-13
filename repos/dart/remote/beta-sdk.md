## `dart:beta-sdk`

```console
$ docker pull dart@sha256:6d793bed7f9b234eca94bf6bba9293361e814a7d77b5e4031a8a46ecfb25f952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:d835f4968cc8be2f357ca4e8ca1afb5aa8889dbf70379a624284665a15ddba7e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286083982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233d25ba78e1cc9afcc44cfe9760fdc806e8fed3b5c49d5638d2c73cf36b4be1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Wed, 12 Jan 2022 22:19:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d2b4ccf63b9160354d63cce1dfd1b47134433047efeb612e2a6373b8d5524bc9;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b3fbb9b5e3c95e2c56d8e0a1d51c841db2908c7afe084842c8e5010a2e45b6f2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=74a9513408c1ab648e93148477f3f59ce609c37289dadd09e83b273369c49fe1;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.16.0-134.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac91afa18c800b262689d7e6a1f9fcc42d0fe8301921811f3dd869be7e7483af`  
		Last Modified: Wed, 12 Jan 2022 22:22:06 GMT  
		Size: 207.0 MB (206987628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:edff47e6282edbac2d158a1b8cefd3615be4a94eb268e76f0497429fcb832190
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192691614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5fca78958e3f58aa9d963ac304acd23ead94b730507804f0536949f1a2cd63`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:00:52 GMT
ADD file:1381e18e2847f24ebd16d8e83ad940adeff45aca2c327d4e07d7451816f29420 in / 
# Tue, 21 Dec 2021 02:00:52 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:31:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:31:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 03:31:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 03:31:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 03:31:50 GMT
WORKDIR /root
# Wed, 12 Jan 2022 22:59:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d2b4ccf63b9160354d63cce1dfd1b47134433047efeb612e2a6373b8d5524bc9;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b3fbb9b5e3c95e2c56d8e0a1d51c841db2908c7afe084842c8e5010a2e45b6f2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=74a9513408c1ab648e93148477f3f59ce609c37289dadd09e83b273369c49fe1;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.16.0-134.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b597e1a6bc27aa2a24a587cb687c9551dfbcfa730a11d48c5a44ff77ff6fdd75`  
		Last Modified: Tue, 21 Dec 2021 02:16:50 GMT  
		Size: 22.8 MB (22754324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724933b2255953150dd8ff394645661fd54951a61361422bd95093fe5e0a5b6f`  
		Last Modified: Tue, 21 Dec 2021 03:34:31 GMT  
		Size: 44.4 MB (44398962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df35a6fcdd7a30ac0a37835fb1e33934c2468b5f30d08368ae3bf49f7bfa461`  
		Last Modified: Tue, 21 Dec 2021 03:34:06 GMT  
		Size: 1.4 MB (1355902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328a35d26f6f1f7e53dda10e87ec55e88016dc3e9231b0e5d9c4ef8f33e0b946`  
		Last Modified: Wed, 12 Jan 2022 23:03:51 GMT  
		Size: 124.2 MB (124182426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d650a6c7614281a9f15ae450194e5b5371d092855e2ea509f7f43231fcb99ef0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.9 MB (202876348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380af4a7762ca51341c7d73630c5e1ce5d5f02e9502476f1c65b66663857b39f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 10:42:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 10:42:06 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 10:42:07 GMT
WORKDIR /root
# Wed, 12 Jan 2022 23:29:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d2b4ccf63b9160354d63cce1dfd1b47134433047efeb612e2a6373b8d5524bc9;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b3fbb9b5e3c95e2c56d8e0a1d51c841db2908c7afe084842c8e5010a2e45b6f2;             SDK_ARCH="arm";;         arm64)             DART_SHA256=74a9513408c1ab648e93148477f3f59ce609c37289dadd09e83b273369c49fe1;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.16.0-134.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727522a568dd0f19904269187584697524c2ca41951cceb1d2c0e2b5cca2b237`  
		Last Modified: Tue, 21 Dec 2021 10:43:15 GMT  
		Size: 49.6 MB (49639004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb72aa07e1e9efbca3d1261e042e1fbe1bb24e1c06e0ec46137338ad38ee1cc`  
		Last Modified: Tue, 21 Dec 2021 10:43:07 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ae246b7664a66bc3c83051c427823cb2f92d1b692b1e27a781f738e97e480d`  
		Last Modified: Wed, 12 Jan 2022 23:30:56 GMT  
		Size: 125.7 MB (125682267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
