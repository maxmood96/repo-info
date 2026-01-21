## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:9ef98ef27ee0a601845820158abf8bb6c750a75c837e08499350d26125cf75a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:0e44b3f4cef5ff128df2cd7bc2b7536735e9ee74e4e23e658a04e1838ec69a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1414888947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d28f3bda6e2b493cff164d6667041a4a8a610c7b833629e7423e014b9a0e472`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:16 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:16 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:49:57 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 15 Jan 2026 22:49:57 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 15 Jan 2026 22:49:57 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Thu, 15 Jan 2026 22:49:57 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 15 Jan 2026 22:49:57 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Thu, 15 Jan 2026 22:49:57 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Thu, 15 Jan 2026 22:49:57 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Thu, 15 Jan 2026 22:49:57 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 15 Jan 2026 22:49:57 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 15 Jan 2026 22:50:36 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Thu, 15 Jan 2026 22:50:36 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:89d3b5863331d6bb79d550bf0acce60aeac36e2c065470bf6d6f8d76c9cb6f4f`  
		Last Modified: Wed, 14 Jan 2026 13:23:48 GMT  
		Size: 62.9 MB (62940156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0dc9418d4c9c444c1037d964ddfbb442f982fefbcfecc2d85599a71b08fca6`  
		Last Modified: Thu, 15 Jan 2026 22:53:01 GMT  
		Size: 326.3 MB (326330735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2201abb0ea65e7852a67d84e018bb8187ec4dae143dee53408da1017be0ff2`  
		Last Modified: Fri, 12 Dec 2025 22:48:01 GMT  
		Size: 1.0 GB (1025617883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30fb857373e044b182be54424bacc31b3c67e115353328bd3b2751975ccb6845`  
		Last Modified: Thu, 15 Jan 2026 22:52:54 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:ef28fe111dbdf8d011e6c9a5c86100b9113b7662da5fddd247f0ba2c240bdced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12734844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887c0359ad14b7ebd6ca700516969dfe544d730296b9b7b1ccdef47233c2eb76`

```dockerfile
```

-	Layers:
	-	`sha256:97e044aff4dccb94d0bd1a7c449b4ac4fa4e9470db0cec1613af2fbe1ba7ad0c`  
		Last Modified: Thu, 15 Jan 2026 22:52:55 GMT  
		Size: 12.7 MB (12719997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa329d9254ae0a5521fc1dc06309de867518748eeabce0c294448a472be9c42e`  
		Last Modified: Thu, 15 Jan 2026 23:51:19 GMT  
		Size: 14.8 KB (14847 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:26ffbf719c2ebfc5beae6f10dd6b529025bfb95625433cd265f2ef98fb2616da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1384536457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3f3ea70b0a750762428bcbd12a4619b2e3806c0d012ef18b7d20c3d887d6c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:03 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:03 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:50:30 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 15 Jan 2026 22:50:30 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 15 Jan 2026 22:50:30 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Thu, 15 Jan 2026 22:50:30 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 15 Jan 2026 22:50:30 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Thu, 15 Jan 2026 22:50:30 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Thu, 15 Jan 2026 22:50:30 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Thu, 15 Jan 2026 22:50:30 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 15 Jan 2026 22:50:30 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 15 Jan 2026 22:51:09 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Thu, 15 Jan 2026 22:51:09 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:afb133ffe3cfc9458fcd28fa75abd002d894e187faa842d48d3c35c676633646`  
		Last Modified: Thu, 15 Jan 2026 07:47:55 GMT  
		Size: 64.8 MB (64770434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bab61b94b2baa2c9c6e409ce91f5e35f0b4424be5cecd0024f66314e19d613`  
		Last Modified: Thu, 15 Jan 2026 22:53:50 GMT  
		Size: 297.7 MB (297676310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843c07ab810a7daa40e66e42b0ca93d3ed6d3ac0199b778324b24d97ed6feac1`  
		Last Modified: Fri, 12 Dec 2025 22:46:44 GMT  
		Size: 1.0 GB (1022089538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5178132fe5551022a06e58be4e5e2971c965723d03741fa2b731ee033c0cb1e`  
		Last Modified: Thu, 15 Jan 2026 22:53:32 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:a2a44de40cf4964f08c167f68b0ed12c15835709632d92702c03207d9f6d243e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12596603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a51fd2f995df0deadcc9909374ba69ce3869d1da68ea879037b35cb9b2d824`

```dockerfile
```

-	Layers:
	-	`sha256:8863877dd55f4b770680da1ab4dd2bebaa959c03cb87f336d0a08c98f47137eb`  
		Last Modified: Thu, 15 Jan 2026 23:51:34 GMT  
		Size: 12.6 MB (12581634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6585c79765b2639905162d7ccabec517f9924815d4ef9106f1cad0374009816`  
		Last Modified: Thu, 15 Jan 2026 23:51:35 GMT  
		Size: 15.0 KB (14969 bytes)  
		MIME: application/vnd.in-toto+json
