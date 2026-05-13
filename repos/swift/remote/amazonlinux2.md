## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:93e7bdfbf45e52cbc8212e5db2d4f4f6c588fdd7d59ac43b67d852897ab8740e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:4331faff4549638668a686b456343df5031707966c42a0fe83b173dcf244c1c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1630960947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3333b6cb58956cbfa8c52b13f14a1154f42bb017daa37a7c6c8c353eef9c042c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:56:20 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:56:20 GMT
CMD ["/bin/bash"]
# Wed, 13 May 2026 18:17:22 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 13 May 2026 18:17:22 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 13 May 2026 18:17:22 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Wed, 13 May 2026 18:17:22 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 13 May 2026 18:17:22 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Wed, 13 May 2026 18:17:22 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Wed, 13 May 2026 18:17:22 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Wed, 13 May 2026 18:17:22 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:17:22 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:18:08 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 13 May 2026 18:18:08 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:3f708fc5705625846e206621966842bfead7ee5b8e4fc20aab0c77c563600126`  
		Last Modified: Wed, 06 May 2026 07:46:46 GMT  
		Size: 62.9 MB (62859738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751ae5fbf92dee081a3fc35d9094a2c11428aa113b121e5495b01e53db7678c9`  
		Last Modified: Wed, 13 May 2026 18:21:06 GMT  
		Size: 331.3 MB (331292517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b3211f73ed6dab4ae86b6305f4bd1df945dcc072033bbff38184751bac5da2`  
		Last Modified: Wed, 13 May 2026 18:21:34 GMT  
		Size: 1.2 GB (1236808518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c96d269a15776d5fa8d5f5c19a86e7725eec16cabf6f3b98dc783c83bae4338`  
		Last Modified: Wed, 13 May 2026 18:20:52 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:de8472cf90299b14c2181bbe34032ab35452efd347a777a5f2635a2206f35804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12734941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc7dd4350763fd6b7337c1a05c1f97765da914cd447a9a6618b4afc00dba416`

```dockerfile
```

-	Layers:
	-	`sha256:961b5141eae545ec8509f05aa87da9420418ad3dd4fee035883e180e6bc53c08`  
		Last Modified: Wed, 13 May 2026 18:20:53 GMT  
		Size: 12.7 MB (12720094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:298c5e70761fc5ae2304f749f9aaecd7afb46048920423430c05bee3f0c349dd`  
		Last Modified: Wed, 13 May 2026 18:20:52 GMT  
		Size: 14.8 KB (14847 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:207aa57820fa20b571a8521aad3553c02458b2f10e485a603d0efb5a8c91bcf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1586836520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce69b7486f18e50a48344eede9284aa2a458397dacf18b8003b5764b3a74d8e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:48:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:14 GMT
CMD ["/bin/bash"]
# Wed, 13 May 2026 18:04:55 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 13 May 2026 18:04:55 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 13 May 2026 18:04:55 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Wed, 13 May 2026 18:04:55 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 13 May 2026 18:04:55 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Wed, 13 May 2026 18:04:55 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Wed, 13 May 2026 18:04:55 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Wed, 13 May 2026 18:04:55 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:04:55 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:05:40 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 13 May 2026 18:05:41 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:835dd3779a793c24eeba54a176badcbf0ecf82042603b5459dd57e14ad679d47`  
		Last Modified: Wed, 06 May 2026 07:46:52 GMT  
		Size: 64.8 MB (64808915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573fae5edbe5d8c4f2d3931a0b11da1cdfc235742f1ad1ab6a82ff0b3d3ba118`  
		Last Modified: Wed, 13 May 2026 18:08:17 GMT  
		Size: 302.4 MB (302435851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d68a9c69fcab24bcd6f286aa786dddc8f06148d2d1aaa2897e551ec726f7608`  
		Last Modified: Wed, 13 May 2026 18:08:41 GMT  
		Size: 1.2 GB (1219591580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a5ced3d8fcd9e1532648fd038616f9994fb2ffefee9e30939a0f721c251d4c`  
		Last Modified: Wed, 13 May 2026 18:08:06 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:e3027f7318275f6c9d772aeb06451f4032cad015d8af18a0318a4d38feae6f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12596700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beab3dec230ac100b12c348740e11a9bc9233fa9fe9ba0aaf2a5d92f7b6fbb7e`

```dockerfile
```

-	Layers:
	-	`sha256:6f5d8ea637fe299415d46aff0cb1505caff12bfc5aa835b93f3dcbe6cac172a3`  
		Last Modified: Wed, 13 May 2026 18:08:06 GMT  
		Size: 12.6 MB (12581731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2df4eeeda0ff42b9d84843a9c4c77a260d32b8d065ab74660b5d05c97aaf4bf4`  
		Last Modified: Wed, 13 May 2026 18:08:06 GMT  
		Size: 15.0 KB (14969 bytes)  
		MIME: application/vnd.in-toto+json
