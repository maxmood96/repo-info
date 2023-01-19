## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:fd33041e2cc8c46bf46692739898ca67ad14eb990018a2f1af53a81278c23f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:1e3a86801d1958e29b8c0c3eb1a85623cf0af136b35a42d716ab8ca423159546
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **897.9 MB (897897377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ab902b773883bb605c23ec8e3da30d7ef4705aa2169f632ce69b4699109f1a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Dec 2022 01:19:49 GMT
ADD file:a69ca7a5499bcd9d6e4317fdbd7256e93be44364bb746f5da10b4268c090bda0 in / 
# Fri, 16 Dec 2022 01:19:50 GMT
CMD ["/bin/bash"]
# Fri, 16 Dec 2022 01:40:03 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 16 Dec 2022 01:40:03 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 16 Dec 2022 01:40:39 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Fri, 16 Dec 2022 01:40:41 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 16 Dec 2022 01:40:41 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Thu, 19 Jan 2023 18:28:11 GMT
ARG SWIFT_BRANCH=swift-5.7.3-release
# Thu, 19 Jan 2023 18:28:11 GMT
ARG SWIFT_VERSION=swift-5.7.3-RELEASE
# Thu, 19 Jan 2023 18:28:11 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 19 Jan 2023 18:28:11 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.7.3-release SWIFT_VERSION=swift-5.7.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 19 Jan 2023 18:28:50 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Thu, 19 Jan 2023 18:28:57 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:5b4a36b5b78f93a5f470cf722b313bb32cddb0f8e0fa0db348059b5c0881b04f`  
		Last Modified: Thu, 15 Dec 2022 23:08:20 GMT  
		Size: 62.3 MB (62328625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419334be1847b87fb236ce143faeb128d763e0ff44fec4799c16624c11034f50`  
		Last Modified: Fri, 16 Dec 2022 02:01:56 GMT  
		Size: 291.4 MB (291409959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73269d6ee3824423814b203762dbbbffa71a3472e95fc3736fc8f65b1bd9ec28`  
		Last Modified: Thu, 19 Jan 2023 18:48:22 GMT  
		Size: 544.2 MB (544158566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c334e6fd745b3b6a085154bb19cfb9fea4e0eec34eb867a90484d211b450e647`  
		Last Modified: Thu, 19 Jan 2023 18:47:05 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:c9c20bc8074a370450b955e66b74e1497f9aba417b5ecdc1eef4a33e4de2dd23
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **839.8 MB (839807715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d77044544ae6bb70ebfdfae9577eaead232025c99200d29762425afc9ccb1a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Dec 2022 00:41:05 GMT
ADD file:26a6bf75c84c408d289e5569f13b1c65206966f875cdfc53ded0670cb85e35bf in / 
# Fri, 16 Dec 2022 00:41:07 GMT
CMD ["/bin/bash"]
# Fri, 16 Dec 2022 01:06:40 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 16 Dec 2022 01:06:40 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 16 Dec 2022 01:07:04 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Fri, 16 Dec 2022 01:07:08 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 16 Dec 2022 01:07:08 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Thu, 19 Jan 2023 18:52:00 GMT
ARG SWIFT_BRANCH=swift-5.7.3-release
# Thu, 19 Jan 2023 18:52:00 GMT
ARG SWIFT_VERSION=swift-5.7.3-RELEASE
# Thu, 19 Jan 2023 18:52:00 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 19 Jan 2023 18:52:00 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.7.3-release SWIFT_VERSION=swift-5.7.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 19 Jan 2023 18:52:37 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Thu, 19 Jan 2023 18:52:49 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:6cbfee25f0741b3d3f4d2474d904a200cd8404a01aa17813bf3fc3d4ebb551a4`  
		Last Modified: Thu, 15 Dec 2022 23:08:20 GMT  
		Size: 64.0 MB (63964214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eab2bc1bb2e8f071a5e921d5b51f892c959bab31ea1a83b3f8a45c21b796848`  
		Last Modified: Fri, 16 Dec 2022 01:11:39 GMT  
		Size: 251.5 MB (251481694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12a9098fd801f51ba39d95e0aa7a20f2bda24a3732622fbf18f73b601ee5d2e`  
		Last Modified: Thu, 19 Jan 2023 18:58:30 GMT  
		Size: 524.4 MB (524361579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c970a18bf65beed60b248bde2beb4c6f89147f839cc5e0129ebd5713a5e7c6`  
		Last Modified: Thu, 19 Jan 2023 18:57:35 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
