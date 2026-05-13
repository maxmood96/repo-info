## `swift:amazonlinux2023`

```console
$ docker pull swift@sha256:b9302e3bc546eb45bc3de5ce366bf5b0d4b5b0d98c1f1734882db3b5e16b1f4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2023` - linux; amd64

```console
$ docker pull swift@sha256:10f610e1b52b0911ca8b11223dcb4d60820e26025d9da7648fa6a0c3f2561062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1469700380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eab710e8f283e7a273499e756ecec7ffd925f57637916fb331146127b884fee`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:55:56 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:55:56 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:19:55 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 09 May 2026 00:19:55 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 09 May 2026 00:19:55 GMT
RUN dnf -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata # buildkit
# Sat, 09 May 2026 00:19:58 GMT
RUN dnf -y swap gnupg2-minimal gnupg2-full # buildkit
# Sat, 09 May 2026 00:19:58 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Sat, 09 May 2026 00:19:58 GMT
ARG SWIFT_PLATFORM=amazonlinux2023
# Sat, 09 May 2026 00:19:58 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Sat, 09 May 2026 00:19:58 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Sat, 09 May 2026 00:19:58 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 09 May 2026 00:19:58 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 09 May 2026 00:20:36 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Sat, 09 May 2026 00:20:36 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:c6daf6f5f632799e37bfaf0ead2057112cc6402948c88e815dfb2bb78f8f7aa1`  
		Last Modified: Tue, 05 May 2026 12:54:11 GMT  
		Size: 54.6 MB (54576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4151fd830b86dd0970a4f070ce4c46b12348338acedba443b1f0ee4c2aabad31`  
		Last Modified: Sat, 09 May 2026 00:23:14 GMT  
		Size: 271.8 MB (271778100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b6390f5629e9e4c4d91ad1f811169ab329856e64908263edd653b43437e001`  
		Last Modified: Sat, 09 May 2026 00:23:09 GMT  
		Size: 23.8 MB (23797653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509f13cc778a767668a55d9c211eea58182be256f51344c23464ebb3329f2d7c`  
		Last Modified: Mon, 20 Apr 2026 21:56:08 GMT  
		Size: 1.1 GB (1119547649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f84d49f9af20f27080b72125144d989ef981398b24e6364320d074fa2d2e6c2`  
		Last Modified: Sat, 09 May 2026 00:23:08 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2023` - unknown; unknown

```console
$ docker pull swift@sha256:0ccdd501e2d2edc7f3ff3e6b88f4ac4f9696c70a03ee8c5dd39e4da299ab0a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13807386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ad1bec2d671c96e19cf9cfc9515e4f072b00c985deb6087013ea33ceac9a29`

```dockerfile
```

-	Layers:
	-	`sha256:dcbce4c75bc19ab68ef6a8c70f3c02bbf116dd49a5320cc05226bcad7bfa042b`  
		Last Modified: Sat, 09 May 2026 00:23:09 GMT  
		Size: 13.8 MB (13791159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:059dce5945e892b45b4dc38b29a5822ea240f25d9295002751fab37e1d4f6191`  
		Last Modified: Sat, 09 May 2026 00:23:08 GMT  
		Size: 16.2 KB (16227 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2023` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:37b9a14b8496b3f8407d3109f2491c6d1cdc204c2e097e441cc426bd9b8dafd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1451629392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b518defd756f4b82ba55b80506f9ec37aa83b9ff1a6478aacbe65e9fc2030c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:48:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:12 GMT
CMD ["/bin/bash"]
# Wed, 13 May 2026 18:05:06 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 13 May 2026 18:05:06 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 13 May 2026 18:05:06 GMT
RUN dnf -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata # buildkit
# Wed, 13 May 2026 18:05:09 GMT
RUN dnf -y swap gnupg2-minimal gnupg2-full # buildkit
# Wed, 13 May 2026 18:05:09 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 13 May 2026 18:05:09 GMT
ARG SWIFT_PLATFORM=amazonlinux2023
# Wed, 13 May 2026 18:05:09 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Wed, 13 May 2026 18:05:09 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Wed, 13 May 2026 18:05:09 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:05:09 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:05:46 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 13 May 2026 18:05:46 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:8ce1f9c92d5e473d6cc57893a4bae88accbdce44b631fbe2bb3a1d2975254fab`  
		Last Modified: Tue, 05 May 2026 12:54:04 GMT  
		Size: 53.5 MB (53456975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f4d403552f91829c2eeceb35fef29310d8ca3d80af0b06340cb276fb08be05`  
		Last Modified: Wed, 13 May 2026 18:08:15 GMT  
		Size: 263.3 MB (263306725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcc2791b6b0bb4d0eb7cd0863567439f08b16a00fbc3e1ee40facfcc080a464`  
		Last Modified: Wed, 13 May 2026 18:08:07 GMT  
		Size: 23.4 MB (23444093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732e2f8c819c0db9ad335e0ab6fd5c6681e1b0183481e5d714d48b72e8537ba4`  
		Last Modified: Wed, 13 May 2026 18:08:33 GMT  
		Size: 1.1 GB (1111421425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f716c14f72388f133c5799526a6f8077a887f64b241c7f3e3c4c695cfd6f0d6e`  
		Last Modified: Wed, 13 May 2026 18:08:05 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2023` - unknown; unknown

```console
$ docker pull swift@sha256:9eef9137a6c3c1dcd717f9b122d5245a17a6c939d8da8dfdf1ce9d0381dd3d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13677575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d3bf5fb68192f1a9e54fd2326752a2db7a30ddd36436ee5c80c046496d7b8c`

```dockerfile
```

-	Layers:
	-	`sha256:4781c87ea342293d3a3db400fd432c21cd4d2a1508b51cd5fd5d3c4d095ab857`  
		Last Modified: Wed, 13 May 2026 18:08:06 GMT  
		Size: 13.7 MB (13661212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b5d63181e3f94d2d7989bec393b89cb385bbd4c9039c50bc743cfe0b210e078`  
		Last Modified: Wed, 13 May 2026 18:08:05 GMT  
		Size: 16.4 KB (16363 bytes)  
		MIME: application/vnd.in-toto+json
