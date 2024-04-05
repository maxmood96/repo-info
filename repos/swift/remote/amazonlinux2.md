## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:1e1c0d7a659f5917bf84eb4fc859657937edc733e5c02a3744da7b555d3ec4f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:839332f3455818002e5b9fc70882e6c0b73ecd770772e857aa849bfb1973b8c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **989.2 MB (989175167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10d22d5ad8952a6c1a2eb84dc751dda077b238a1a3d21ff83965f10776eb091`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 05 Apr 2024 18:22:03 GMT
COPY dir:9acefc3d435d9504bd7fba575b2c4ee96a407449bf3ba0c2338d49d9a97b2a5a in / 
# Fri, 05 Apr 2024 18:22:04 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 18:38:44 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 05 Apr 2024 18:38:44 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 05 Apr 2024 18:39:15 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Fri, 05 Apr 2024 18:39:17 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 05 Apr 2024 18:39:17 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 05 Apr 2024 18:39:17 GMT
ARG SWIFT_BRANCH=swift-5.10-release
# Fri, 05 Apr 2024 18:39:17 GMT
ARG SWIFT_VERSION=swift-5.10-RELEASE
# Fri, 05 Apr 2024 18:39:17 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 05 Apr 2024 18:39:17 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.10-release SWIFT_VERSION=swift-5.10-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 05 Apr 2024 18:39:56 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Fri, 05 Apr 2024 18:40:03 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:b48a4417297666404bb1459ef5f08938bfff21f2d5adb051db9f61fc54934d30`  
		Last Modified: Wed, 03 Apr 2024 01:52:33 GMT  
		Size: 62.7 MB (62667250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b1beba61f81fbd484e96b90d83243b14be85350a84acd54f0a24325becab17`  
		Last Modified: Fri, 05 Apr 2024 18:58:24 GMT  
		Size: 302.2 MB (302150834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9955acb73bff9784aa3c7caf666e555a7056c4c49d17de166be92876b2ec168a`  
		Last Modified: Fri, 05 Apr 2024 18:59:15 GMT  
		Size: 624.4 MB (624356885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4756fa3539b58b98578d818efc23fba880397871af907ee4197834ae8d6100`  
		Last Modified: Fri, 05 Apr 2024 18:57:48 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:790510f2c68ae049285ba7cd15f17674ba554f5414ea5ace03309ce95b8b87eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **950.7 MB (950667130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fcad64364b62468b4d550809f9aa05a8ee415317a9c7321f4e2d8f2be986fd6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 05 Apr 2024 18:07:30 GMT
COPY dir:5c5e76fbf44d4b5d5bbd02274337780df6faf67a7b224750d628854242527355 in / 
# Fri, 05 Apr 2024 18:07:31 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 18:26:14 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 05 Apr 2024 18:26:14 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 05 Apr 2024 18:26:39 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Fri, 05 Apr 2024 18:26:44 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 05 Apr 2024 18:26:44 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 05 Apr 2024 18:26:44 GMT
ARG SWIFT_BRANCH=swift-5.10-release
# Fri, 05 Apr 2024 18:26:44 GMT
ARG SWIFT_VERSION=swift-5.10-RELEASE
# Fri, 05 Apr 2024 18:26:44 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 05 Apr 2024 18:26:44 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.10-release SWIFT_VERSION=swift-5.10-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 05 Apr 2024 18:27:24 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Fri, 05 Apr 2024 18:27:37 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:1e9d4daaed12ccc925403048e4968011b475e192de72d80e36180798aac508fa`  
		Last Modified: Wed, 03 Apr 2024 01:52:31 GMT  
		Size: 64.6 MB (64560609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cb953c4944512c11c592f235cd7e69112b9a842347cfaf1b5c8bbb3b708f8c`  
		Last Modified: Fri, 05 Apr 2024 18:36:02 GMT  
		Size: 268.4 MB (268412484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4c8ecede3056b45dbe1f169c2a996a83a046d48009b58f47889b064334132d`  
		Last Modified: Fri, 05 Apr 2024 18:36:39 GMT  
		Size: 617.7 MB (617693838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10c5cc0431df21e5fcb18b584e3db0baa369ee735160b0000cf6b8719f59557`  
		Last Modified: Fri, 05 Apr 2024 18:35:37 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
