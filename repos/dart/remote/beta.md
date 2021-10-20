## `dart:beta`

```console
$ docker pull dart@sha256:c34151403ff481d4aaed6fe8c37ed7c734d59f28e20daaa97abfcabe105cce6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:1e834c5b3ac48873d4e4f99c67190b9b69f3f0cc40c322022e358182b2d311d4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.5 MB (283518094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed02f1aa7243085b858078bf198f9efcdba4580c592947114f6affeb977e0e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 09:48:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 09:48:59 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 12 Oct 2021 09:49:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 12 Oct 2021 09:49:00 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 09:49:00 GMT
WORKDIR /root
# Thu, 14 Oct 2021 19:28:27 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.15.0-178.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "0aa79c07ab059598b434fce574591ea5e318aefc579b3fe0b27e985fc5159270 *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0967f1c7a0cff360e1b4b316d95f992ede8dd65a5ce3d015aeabaad78b097d`  
		Last Modified: Tue, 12 Oct 2021 09:50:01 GMT  
		Size: 49.6 MB (49582550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b872aeb4f5e62a618c7ffe96a15e50654b6f1cbf9539b6756b5302f93a0c928`  
		Last Modified: Tue, 12 Oct 2021 09:49:53 GMT  
		Size: 2.4 MB (2359146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4bf4f85067b9e35650da7552b89eefe58e1ae9d153c8ebfa03461518a1fc01`  
		Last Modified: Thu, 14 Oct 2021 19:30:14 GMT  
		Size: 204.4 MB (204436888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0d945a09fef62899d1ef30131b04be7b7b1eb441b14b63376465c8daa4bb7e9a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.2 MB (197212148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f6031f6db9582006f1afc39172494972e33c34fb8670ddda07ff940a5d3b41`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:41:42 GMT
ADD file:f0d53027a7ba594477674127971aa477af3a2bc6bcddef6c0aa174953a5f2db0 in / 
# Tue, 12 Oct 2021 01:41:42 GMT
CMD ["bash"]
# Wed, 20 Oct 2021 18:44:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Oct 2021 18:44:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 20 Oct 2021 18:44:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Oct 2021 18:44:25 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Oct 2021 18:44:26 GMT
WORKDIR /root
# Wed, 20 Oct 2021 18:44:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0aa79c07ab059598b434fce574591ea5e318aefc579b3fe0b27e985fc5159270;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4d0e0b9c0f30ecc2f65c4ff786948d99a06fa42a9191fe3be63efc56d40bafae;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e62e1ad98ada15b694641868c6d78c984796a12fcad74635db3527844130c875;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.15.0-178.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:02b45931a436a68cadb742684148ed6aacbbf9aa21447b467c11bac97f92eb46`  
		Last Modified: Tue, 12 Oct 2021 01:49:07 GMT  
		Size: 25.9 MB (25908479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a55ddd8113ef38d17d67a4104cede247dccdae5d82c759bb8200adf5dd79777`  
		Last Modified: Wed, 20 Oct 2021 18:45:38 GMT  
		Size: 49.6 MB (49638983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02dbc39b6a737a104b6c9a67ea9ed2c9e533d43dd1c9fb0d8d2eb1c5a3273e10`  
		Last Modified: Wed, 20 Oct 2021 18:45:32 GMT  
		Size: 1.6 MB (1631930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd00b24f014687c9c00622da7a593f02d4a39ad305787ca3d2a531dbf767da9c`  
		Last Modified: Wed, 20 Oct 2021 18:46:40 GMT  
		Size: 120.0 MB (120032756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
