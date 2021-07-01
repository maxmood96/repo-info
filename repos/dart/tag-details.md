<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:2`](#dart2)
-	[`dart:2-sdk`](#dart2-sdk)
-	[`dart:2.13`](#dart213)
-	[`dart:2.13-sdk`](#dart213-sdk)
-	[`dart:2.13.4`](#dart2134)
-	[`dart:2.13.4-sdk`](#dart2134-sdk)
-	[`dart:2.14.0-188.5.beta`](#dart2140-1885beta)
-	[`dart:2.14.0-188.5.beta-sdk`](#dart2140-1885beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:2`

```console
$ docker pull dart@sha256:c069b45c0c11a76b575e05394481615ba9ce504e3aba819e6d499f75c1585f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `dart:2` - linux; amd64

```console
$ docker pull dart@sha256:4880f55f0bb74ef86d657fb06d3fe8ca8c58740d2f074b1de91400fac2e408e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.8 MB (274814350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5008f7d4eec44c31c4ecab82944e6f5e6065e1a1aae38406fd8af800d9a0b2d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 01:06:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 01:06:29 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 23 Jun 2021 01:06:29 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 23 Jun 2021 01:06:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 01:06:30 GMT
WORKDIR /root
# Wed, 30 Jun 2021 17:19:51 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.13.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "633a9aa4812b725ff587e2bbf16cd5839224cfe05dcd536e1a74804e80fdb4cd *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d99d90875f908f3ddefbd327b783a5f2248120e1e2705cac3bd6ebd7c539161`  
		Last Modified: Wed, 23 Jun 2021 01:07:45 GMT  
		Size: 49.6 MB (49581346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493f9addfbfff0f2f9bf193943ea63eb7628fb005687df66ea54cf1421f3117a`  
		Last Modified: Wed, 23 Jun 2021 01:07:34 GMT  
		Size: 2.4 MB (2359144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564fda40737fba87097508f7988d229a32f9ee1fb915b1ab2b1c457d9168da33`  
		Last Modified: Wed, 30 Jun 2021 17:21:02 GMT  
		Size: 195.7 MB (195728009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2-sdk`

```console
$ docker pull dart@sha256:c069b45c0c11a76b575e05394481615ba9ce504e3aba819e6d499f75c1585f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `dart:2-sdk` - linux; amd64

```console
$ docker pull dart@sha256:4880f55f0bb74ef86d657fb06d3fe8ca8c58740d2f074b1de91400fac2e408e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.8 MB (274814350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5008f7d4eec44c31c4ecab82944e6f5e6065e1a1aae38406fd8af800d9a0b2d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 01:06:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 01:06:29 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 23 Jun 2021 01:06:29 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 23 Jun 2021 01:06:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 01:06:30 GMT
WORKDIR /root
# Wed, 30 Jun 2021 17:19:51 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.13.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "633a9aa4812b725ff587e2bbf16cd5839224cfe05dcd536e1a74804e80fdb4cd *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d99d90875f908f3ddefbd327b783a5f2248120e1e2705cac3bd6ebd7c539161`  
		Last Modified: Wed, 23 Jun 2021 01:07:45 GMT  
		Size: 49.6 MB (49581346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493f9addfbfff0f2f9bf193943ea63eb7628fb005687df66ea54cf1421f3117a`  
		Last Modified: Wed, 23 Jun 2021 01:07:34 GMT  
		Size: 2.4 MB (2359144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564fda40737fba87097508f7988d229a32f9ee1fb915b1ab2b1c457d9168da33`  
		Last Modified: Wed, 30 Jun 2021 17:21:02 GMT  
		Size: 195.7 MB (195728009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.13`

```console
$ docker pull dart@sha256:c069b45c0c11a76b575e05394481615ba9ce504e3aba819e6d499f75c1585f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `dart:2.13` - linux; amd64

```console
$ docker pull dart@sha256:4880f55f0bb74ef86d657fb06d3fe8ca8c58740d2f074b1de91400fac2e408e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.8 MB (274814350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5008f7d4eec44c31c4ecab82944e6f5e6065e1a1aae38406fd8af800d9a0b2d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 01:06:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 01:06:29 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 23 Jun 2021 01:06:29 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 23 Jun 2021 01:06:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 01:06:30 GMT
WORKDIR /root
# Wed, 30 Jun 2021 17:19:51 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.13.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "633a9aa4812b725ff587e2bbf16cd5839224cfe05dcd536e1a74804e80fdb4cd *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d99d90875f908f3ddefbd327b783a5f2248120e1e2705cac3bd6ebd7c539161`  
		Last Modified: Wed, 23 Jun 2021 01:07:45 GMT  
		Size: 49.6 MB (49581346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493f9addfbfff0f2f9bf193943ea63eb7628fb005687df66ea54cf1421f3117a`  
		Last Modified: Wed, 23 Jun 2021 01:07:34 GMT  
		Size: 2.4 MB (2359144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564fda40737fba87097508f7988d229a32f9ee1fb915b1ab2b1c457d9168da33`  
		Last Modified: Wed, 30 Jun 2021 17:21:02 GMT  
		Size: 195.7 MB (195728009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.13-sdk`

```console
$ docker pull dart@sha256:c069b45c0c11a76b575e05394481615ba9ce504e3aba819e6d499f75c1585f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `dart:2.13-sdk` - linux; amd64

```console
$ docker pull dart@sha256:4880f55f0bb74ef86d657fb06d3fe8ca8c58740d2f074b1de91400fac2e408e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.8 MB (274814350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5008f7d4eec44c31c4ecab82944e6f5e6065e1a1aae38406fd8af800d9a0b2d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 01:06:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 01:06:29 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 23 Jun 2021 01:06:29 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 23 Jun 2021 01:06:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 01:06:30 GMT
WORKDIR /root
# Wed, 30 Jun 2021 17:19:51 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.13.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "633a9aa4812b725ff587e2bbf16cd5839224cfe05dcd536e1a74804e80fdb4cd *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d99d90875f908f3ddefbd327b783a5f2248120e1e2705cac3bd6ebd7c539161`  
		Last Modified: Wed, 23 Jun 2021 01:07:45 GMT  
		Size: 49.6 MB (49581346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493f9addfbfff0f2f9bf193943ea63eb7628fb005687df66ea54cf1421f3117a`  
		Last Modified: Wed, 23 Jun 2021 01:07:34 GMT  
		Size: 2.4 MB (2359144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564fda40737fba87097508f7988d229a32f9ee1fb915b1ab2b1c457d9168da33`  
		Last Modified: Wed, 30 Jun 2021 17:21:02 GMT  
		Size: 195.7 MB (195728009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.13.4`

```console
$ docker pull dart@sha256:c069b45c0c11a76b575e05394481615ba9ce504e3aba819e6d499f75c1585f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `dart:2.13.4` - linux; amd64

```console
$ docker pull dart@sha256:4880f55f0bb74ef86d657fb06d3fe8ca8c58740d2f074b1de91400fac2e408e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.8 MB (274814350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5008f7d4eec44c31c4ecab82944e6f5e6065e1a1aae38406fd8af800d9a0b2d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 01:06:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 01:06:29 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 23 Jun 2021 01:06:29 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 23 Jun 2021 01:06:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 01:06:30 GMT
WORKDIR /root
# Wed, 30 Jun 2021 17:19:51 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.13.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "633a9aa4812b725ff587e2bbf16cd5839224cfe05dcd536e1a74804e80fdb4cd *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d99d90875f908f3ddefbd327b783a5f2248120e1e2705cac3bd6ebd7c539161`  
		Last Modified: Wed, 23 Jun 2021 01:07:45 GMT  
		Size: 49.6 MB (49581346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493f9addfbfff0f2f9bf193943ea63eb7628fb005687df66ea54cf1421f3117a`  
		Last Modified: Wed, 23 Jun 2021 01:07:34 GMT  
		Size: 2.4 MB (2359144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564fda40737fba87097508f7988d229a32f9ee1fb915b1ab2b1c457d9168da33`  
		Last Modified: Wed, 30 Jun 2021 17:21:02 GMT  
		Size: 195.7 MB (195728009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.13.4-sdk`

```console
$ docker pull dart@sha256:c069b45c0c11a76b575e05394481615ba9ce504e3aba819e6d499f75c1585f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `dart:2.13.4-sdk` - linux; amd64

```console
$ docker pull dart@sha256:4880f55f0bb74ef86d657fb06d3fe8ca8c58740d2f074b1de91400fac2e408e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.8 MB (274814350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5008f7d4eec44c31c4ecab82944e6f5e6065e1a1aae38406fd8af800d9a0b2d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 01:06:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 01:06:29 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 23 Jun 2021 01:06:29 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 23 Jun 2021 01:06:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 01:06:30 GMT
WORKDIR /root
# Wed, 30 Jun 2021 17:19:51 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.13.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "633a9aa4812b725ff587e2bbf16cd5839224cfe05dcd536e1a74804e80fdb4cd *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d99d90875f908f3ddefbd327b783a5f2248120e1e2705cac3bd6ebd7c539161`  
		Last Modified: Wed, 23 Jun 2021 01:07:45 GMT  
		Size: 49.6 MB (49581346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493f9addfbfff0f2f9bf193943ea63eb7628fb005687df66ea54cf1421f3117a`  
		Last Modified: Wed, 23 Jun 2021 01:07:34 GMT  
		Size: 2.4 MB (2359144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564fda40737fba87097508f7988d229a32f9ee1fb915b1ab2b1c457d9168da33`  
		Last Modified: Wed, 30 Jun 2021 17:21:02 GMT  
		Size: 195.7 MB (195728009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.14.0-188.5.beta`

```console
$ docker pull dart@sha256:5860d9af62671a0a7651217f8838de3f8080db729e242855cc88dbe0d3a0d421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `dart:2.14.0-188.5.beta` - linux; amd64

```console
$ docker pull dart@sha256:8f46ace3c39c499f55765d9fdb5392ed86d9cb96f1342b5b1dc256f8df05046a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288872894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67eb3286ebc95e040a8a7f941ed17db429a6739540341ec3c9fe4f8643d32dd3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 01:06:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 01:06:29 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 23 Jun 2021 01:06:29 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 23 Jun 2021 01:06:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 01:06:30 GMT
WORKDIR /root
# Wed, 30 Jun 2021 17:20:13 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.14.0-188.5.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "11c2e3a35e0a13de20e5d88831db69bd7d18c077b10c77cbabd61dc36e473ba7 *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d99d90875f908f3ddefbd327b783a5f2248120e1e2705cac3bd6ebd7c539161`  
		Last Modified: Wed, 23 Jun 2021 01:07:45 GMT  
		Size: 49.6 MB (49581346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493f9addfbfff0f2f9bf193943ea63eb7628fb005687df66ea54cf1421f3117a`  
		Last Modified: Wed, 23 Jun 2021 01:07:34 GMT  
		Size: 2.4 MB (2359144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e8b389b6261d51889a3161e9de6fd6738a9cee8e728f0d4f0d96cfb0615709`  
		Last Modified: Wed, 30 Jun 2021 17:22:02 GMT  
		Size: 209.8 MB (209786553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.14.0-188.5.beta-sdk`

```console
$ docker pull dart@sha256:5860d9af62671a0a7651217f8838de3f8080db729e242855cc88dbe0d3a0d421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `dart:2.14.0-188.5.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:8f46ace3c39c499f55765d9fdb5392ed86d9cb96f1342b5b1dc256f8df05046a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288872894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67eb3286ebc95e040a8a7f941ed17db429a6739540341ec3c9fe4f8643d32dd3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 01:06:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 01:06:29 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 23 Jun 2021 01:06:29 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 23 Jun 2021 01:06:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 01:06:30 GMT
WORKDIR /root
# Wed, 30 Jun 2021 17:20:13 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.14.0-188.5.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "11c2e3a35e0a13de20e5d88831db69bd7d18c077b10c77cbabd61dc36e473ba7 *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d99d90875f908f3ddefbd327b783a5f2248120e1e2705cac3bd6ebd7c539161`  
		Last Modified: Wed, 23 Jun 2021 01:07:45 GMT  
		Size: 49.6 MB (49581346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493f9addfbfff0f2f9bf193943ea63eb7628fb005687df66ea54cf1421f3117a`  
		Last Modified: Wed, 23 Jun 2021 01:07:34 GMT  
		Size: 2.4 MB (2359144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e8b389b6261d51889a3161e9de6fd6738a9cee8e728f0d4f0d96cfb0615709`  
		Last Modified: Wed, 30 Jun 2021 17:22:02 GMT  
		Size: 209.8 MB (209786553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta`

```console
$ docker pull dart@sha256:5860d9af62671a0a7651217f8838de3f8080db729e242855cc88dbe0d3a0d421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:8f46ace3c39c499f55765d9fdb5392ed86d9cb96f1342b5b1dc256f8df05046a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288872894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67eb3286ebc95e040a8a7f941ed17db429a6739540341ec3c9fe4f8643d32dd3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 01:06:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 01:06:29 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 23 Jun 2021 01:06:29 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 23 Jun 2021 01:06:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 01:06:30 GMT
WORKDIR /root
# Wed, 30 Jun 2021 17:20:13 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.14.0-188.5.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "11c2e3a35e0a13de20e5d88831db69bd7d18c077b10c77cbabd61dc36e473ba7 *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d99d90875f908f3ddefbd327b783a5f2248120e1e2705cac3bd6ebd7c539161`  
		Last Modified: Wed, 23 Jun 2021 01:07:45 GMT  
		Size: 49.6 MB (49581346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493f9addfbfff0f2f9bf193943ea63eb7628fb005687df66ea54cf1421f3117a`  
		Last Modified: Wed, 23 Jun 2021 01:07:34 GMT  
		Size: 2.4 MB (2359144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e8b389b6261d51889a3161e9de6fd6738a9cee8e728f0d4f0d96cfb0615709`  
		Last Modified: Wed, 30 Jun 2021 17:22:02 GMT  
		Size: 209.8 MB (209786553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:5860d9af62671a0a7651217f8838de3f8080db729e242855cc88dbe0d3a0d421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:8f46ace3c39c499f55765d9fdb5392ed86d9cb96f1342b5b1dc256f8df05046a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288872894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67eb3286ebc95e040a8a7f941ed17db429a6739540341ec3c9fe4f8643d32dd3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 01:06:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 01:06:29 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 23 Jun 2021 01:06:29 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 23 Jun 2021 01:06:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 01:06:30 GMT
WORKDIR /root
# Wed, 30 Jun 2021 17:20:13 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.14.0-188.5.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "11c2e3a35e0a13de20e5d88831db69bd7d18c077b10c77cbabd61dc36e473ba7 *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d99d90875f908f3ddefbd327b783a5f2248120e1e2705cac3bd6ebd7c539161`  
		Last Modified: Wed, 23 Jun 2021 01:07:45 GMT  
		Size: 49.6 MB (49581346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493f9addfbfff0f2f9bf193943ea63eb7628fb005687df66ea54cf1421f3117a`  
		Last Modified: Wed, 23 Jun 2021 01:07:34 GMT  
		Size: 2.4 MB (2359144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e8b389b6261d51889a3161e9de6fd6738a9cee8e728f0d4f0d96cfb0615709`  
		Last Modified: Wed, 30 Jun 2021 17:22:02 GMT  
		Size: 209.8 MB (209786553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:latest`

```console
$ docker pull dart@sha256:c069b45c0c11a76b575e05394481615ba9ce504e3aba819e6d499f75c1585f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:4880f55f0bb74ef86d657fb06d3fe8ca8c58740d2f074b1de91400fac2e408e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.8 MB (274814350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5008f7d4eec44c31c4ecab82944e6f5e6065e1a1aae38406fd8af800d9a0b2d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 01:06:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 01:06:29 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 23 Jun 2021 01:06:29 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 23 Jun 2021 01:06:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 01:06:30 GMT
WORKDIR /root
# Wed, 30 Jun 2021 17:19:51 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.13.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "633a9aa4812b725ff587e2bbf16cd5839224cfe05dcd536e1a74804e80fdb4cd *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d99d90875f908f3ddefbd327b783a5f2248120e1e2705cac3bd6ebd7c539161`  
		Last Modified: Wed, 23 Jun 2021 01:07:45 GMT  
		Size: 49.6 MB (49581346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493f9addfbfff0f2f9bf193943ea63eb7628fb005687df66ea54cf1421f3117a`  
		Last Modified: Wed, 23 Jun 2021 01:07:34 GMT  
		Size: 2.4 MB (2359144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564fda40737fba87097508f7988d229a32f9ee1fb915b1ab2b1c457d9168da33`  
		Last Modified: Wed, 30 Jun 2021 17:21:02 GMT  
		Size: 195.7 MB (195728009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:sdk`

```console
$ docker pull dart@sha256:c069b45c0c11a76b575e05394481615ba9ce504e3aba819e6d499f75c1585f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:4880f55f0bb74ef86d657fb06d3fe8ca8c58740d2f074b1de91400fac2e408e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.8 MB (274814350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5008f7d4eec44c31c4ecab82944e6f5e6065e1a1aae38406fd8af800d9a0b2d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 01:06:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 01:06:29 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 23 Jun 2021 01:06:29 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 23 Jun 2021 01:06:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 01:06:30 GMT
WORKDIR /root
# Wed, 30 Jun 2021 17:19:51 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.13.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "633a9aa4812b725ff587e2bbf16cd5839224cfe05dcd536e1a74804e80fdb4cd *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d99d90875f908f3ddefbd327b783a5f2248120e1e2705cac3bd6ebd7c539161`  
		Last Modified: Wed, 23 Jun 2021 01:07:45 GMT  
		Size: 49.6 MB (49581346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493f9addfbfff0f2f9bf193943ea63eb7628fb005687df66ea54cf1421f3117a`  
		Last Modified: Wed, 23 Jun 2021 01:07:34 GMT  
		Size: 2.4 MB (2359144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564fda40737fba87097508f7988d229a32f9ee1fb915b1ab2b1c457d9168da33`  
		Last Modified: Wed, 30 Jun 2021 17:21:02 GMT  
		Size: 195.7 MB (195728009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable`

```console
$ docker pull dart@sha256:c069b45c0c11a76b575e05394481615ba9ce504e3aba819e6d499f75c1585f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:4880f55f0bb74ef86d657fb06d3fe8ca8c58740d2f074b1de91400fac2e408e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.8 MB (274814350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5008f7d4eec44c31c4ecab82944e6f5e6065e1a1aae38406fd8af800d9a0b2d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 01:06:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 01:06:29 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 23 Jun 2021 01:06:29 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 23 Jun 2021 01:06:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 01:06:30 GMT
WORKDIR /root
# Wed, 30 Jun 2021 17:19:51 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.13.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "633a9aa4812b725ff587e2bbf16cd5839224cfe05dcd536e1a74804e80fdb4cd *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d99d90875f908f3ddefbd327b783a5f2248120e1e2705cac3bd6ebd7c539161`  
		Last Modified: Wed, 23 Jun 2021 01:07:45 GMT  
		Size: 49.6 MB (49581346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493f9addfbfff0f2f9bf193943ea63eb7628fb005687df66ea54cf1421f3117a`  
		Last Modified: Wed, 23 Jun 2021 01:07:34 GMT  
		Size: 2.4 MB (2359144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564fda40737fba87097508f7988d229a32f9ee1fb915b1ab2b1c457d9168da33`  
		Last Modified: Wed, 30 Jun 2021 17:21:02 GMT  
		Size: 195.7 MB (195728009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:c069b45c0c11a76b575e05394481615ba9ce504e3aba819e6d499f75c1585f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:4880f55f0bb74ef86d657fb06d3fe8ca8c58740d2f074b1de91400fac2e408e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.8 MB (274814350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5008f7d4eec44c31c4ecab82944e6f5e6065e1a1aae38406fd8af800d9a0b2d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 01:06:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 01:06:29 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 23 Jun 2021 01:06:29 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 23 Jun 2021 01:06:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 01:06:30 GMT
WORKDIR /root
# Wed, 30 Jun 2021 17:19:51 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.13.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "633a9aa4812b725ff587e2bbf16cd5839224cfe05dcd536e1a74804e80fdb4cd *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d99d90875f908f3ddefbd327b783a5f2248120e1e2705cac3bd6ebd7c539161`  
		Last Modified: Wed, 23 Jun 2021 01:07:45 GMT  
		Size: 49.6 MB (49581346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493f9addfbfff0f2f9bf193943ea63eb7628fb005687df66ea54cf1421f3117a`  
		Last Modified: Wed, 23 Jun 2021 01:07:34 GMT  
		Size: 2.4 MB (2359144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564fda40737fba87097508f7988d229a32f9ee1fb915b1ab2b1c457d9168da33`  
		Last Modified: Wed, 30 Jun 2021 17:21:02 GMT  
		Size: 195.7 MB (195728009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
