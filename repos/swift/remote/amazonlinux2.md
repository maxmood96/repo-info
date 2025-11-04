## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:d20e759bf05afd98b0e32b08f738b1d7da7554c01240773edc0d94e45b477dcf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:c8d6896c3b0293f1696d8934564a0f68d097a981f804d4fae7d73130bc27d94c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1411486206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aaac61709325d8d18be3cf8e0a33c024f95be37f079d097b23ae2f6f3ce8965`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:45 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:13:01 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 31 Oct 2025 00:13:01 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 31 Oct 2025 00:13:01 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Fri, 31 Oct 2025 00:13:01 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 31 Oct 2025 00:13:01 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 31 Oct 2025 00:13:01 GMT
ARG SWIFT_BRANCH=swift-6.2-release
# Fri, 31 Oct 2025 00:13:01 GMT
ARG SWIFT_VERSION=swift-6.2-RELEASE
# Fri, 31 Oct 2025 00:13:01 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 31 Oct 2025 00:13:01 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 31 Oct 2025 00:13:41 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Fri, 31 Oct 2025 00:13:41 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:2e3ea9592aad33f5f11ca8c65604905de30de68b0c38dfad7dee51b605c2a2c5`  
		Last Modified: Thu, 30 Oct 2025 03:52:34 GMT  
		Size: 62.9 MB (62934068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33422a1e739aa7d4fc3f2c09120c673d23c073807c335fd4ea1c50f35ac864e0`  
		Last Modified: Fri, 31 Oct 2025 01:52:42 GMT  
		Size: 323.7 MB (323749493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb227f8b0cca243b4649727bca666fe0c4713ddc1823e4de7fa8f61adf08f3b`  
		Last Modified: Tue, 16 Sep 2025 20:07:42 GMT  
		Size: 1.0 GB (1024802471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad620f6a1d7b6d5217eb185bc3668dc1afa21748ab6f7252c541ef1d1c21d90`  
		Last Modified: Fri, 31 Oct 2025 00:16:21 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:2689b3d7491715ff30ca1fa6026fe5a03dd296a254349a4a8983a9a0aa235391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12734821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5559506273d79b8c1b594ac10ab083c2b3dd6f715076823d4a1372ac5ef0a520`

```dockerfile
```

-	Layers:
	-	`sha256:daea5db91c345fb962447c6d73cf529e8a092cf33d9d9bd005f2bccc3559046f`  
		Last Modified: Fri, 31 Oct 2025 01:48:38 GMT  
		Size: 12.7 MB (12719987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c4ff01455517cd9e839ef4d3a8f358099a9bfa0f6af9699457e31989e623518`  
		Last Modified: Fri, 31 Oct 2025 01:48:39 GMT  
		Size: 14.8 KB (14834 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:1d1ef4ac973848bab345c0fedd18c6887f4d5a3ed658e06038aa920008df78da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1382018845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4317cbc46bc483283fc9c8a6941b9244d49a3ff1a37bd96791bb3e8db3471ff8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:47 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:47 GMT
CMD ["/bin/bash"]
# Tue, 04 Nov 2025 19:24:22 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 04 Nov 2025 19:24:22 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 04 Nov 2025 19:24:22 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Tue, 04 Nov 2025 19:24:22 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 04 Nov 2025 19:24:22 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 04 Nov 2025 19:24:22 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Tue, 04 Nov 2025 19:24:22 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Tue, 04 Nov 2025 19:24:22 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 19:24:22 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 19:25:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Tue, 04 Nov 2025 19:25:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:2875a69d1768080ef2331610c2aea8f8cfff54b5df360eb9feb01240a7526ff5`  
		Last Modified: Thu, 30 Oct 2025 23:15:16 GMT  
		Size: 64.8 MB (64793458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fc5998476632e29e649fdf28d3cc4f0409b176711c51692c2498e129e985e8`  
		Last Modified: Tue, 04 Nov 2025 20:51:41 GMT  
		Size: 295.3 MB (295317180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530e29bfe332d82339a65c057a82781c6f50e73f0e5fb0d5d316eea41f376e45`  
		Last Modified: Tue, 04 Nov 2025 20:52:07 GMT  
		Size: 1.0 GB (1021908034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb60809d5c706cf4f930bbb612bc1a2f01ac843d07c8189d9861183101ab72b`  
		Last Modified: Tue, 04 Nov 2025 19:27:38 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:86a0080e53bbe681ef42ca6339f6184d085a2caebef9548797d38c1bbaf025ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12596597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76cb75a74a69dddb0f0eaca6849411827e65cac8dc43790eeda4012987384dfd`

```dockerfile
```

-	Layers:
	-	`sha256:6a8e2cd47693c62058b0a5b4ed8093061d2ea9574eff21d60a5770b5e93c84e1`  
		Last Modified: Tue, 04 Nov 2025 20:48:02 GMT  
		Size: 12.6 MB (12581628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c13bc22ac1a43b6cfe2c5de8e2a0bca0fe61794cb6aa8bd07e79fe58084453c3`  
		Last Modified: Tue, 04 Nov 2025 20:48:03 GMT  
		Size: 15.0 KB (14969 bytes)  
		MIME: application/vnd.in-toto+json
