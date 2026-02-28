## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:9c49563ad620a191db6ea4f5252699188cc4c302c0d6cfae550e0434cedf3e50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:df5dfa1c9cf60d8dfeb0024e1fde2940dbb7cd2c6356b17b92db9d634bd2c0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286208279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f626bdc2b7cc6cf5bb52c12c3a1e98ac0ccbdfb4cda2f88020427bfef97795ff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:14:13 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:14:13 GMT
CMD ["/bin/bash"]
# Fri, 27 Feb 2026 22:44:47 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 27 Feb 2026 22:44:47 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 27 Feb 2026 22:44:47 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 27 Feb 2026 22:44:47 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 27 Feb 2026 22:44:47 GMT
ARG SWIFT_BRANCH=swift-6.2.4-release
# Fri, 27 Feb 2026 22:44:47 GMT
ARG SWIFT_VERSION=swift-6.2.4-RELEASE
# Fri, 27 Feb 2026 22:44:47 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 27 Feb 2026 22:44:47 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 27 Feb 2026 22:44:47 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:f5abe3fbfd395e17e5203e7213ac7dbf150f56cd98e8268563339f7d27569870`  
		Last Modified: Tue, 10 Feb 2026 14:46:03 GMT  
		Size: 63.0 MB (62958957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ec72c6f643533bc9476b01a005925dbdb9d434dd09791a492f4214e10204b7`  
		Last Modified: Fri, 27 Feb 2026 22:45:18 GMT  
		Size: 223.2 MB (223249322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:4aa1863538541acbd8fc57333bf1f61e603a55856754b264b3ccfdee21c51ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9553b7a787ea492d27ada77b35879bbece5eb488b10768944f4bfa85eaf598dd`

```dockerfile
```

-	Layers:
	-	`sha256:824c9c23907a93e44c9b50b0a401d9341724c69720884ca269cbe97ada46f403`  
		Last Modified: Fri, 27 Feb 2026 22:45:13 GMT  
		Size: 5.1 MB (5082197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e020c19edcc98c1874de09b08d95804aa583f22e998ca64adb6f5757cd446cd`  
		Last Modified: Fri, 27 Feb 2026 22:45:13 GMT  
		Size: 11.9 KB (11854 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:ddecd6b405e06ce43cfa19d227e9bda7ccd9b3debbca8645fcbc5ae1f74c943e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263242890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce857283816ef5e125280ec438f1f9b866308be9e9361289af8b54e61d27a8a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:14:03 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:14:03 GMT
CMD ["/bin/bash"]
# Fri, 27 Feb 2026 22:43:24 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 27 Feb 2026 22:43:24 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 27 Feb 2026 22:43:24 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 27 Feb 2026 22:43:24 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 27 Feb 2026 22:43:24 GMT
ARG SWIFT_BRANCH=swift-6.2.4-release
# Fri, 27 Feb 2026 22:43:24 GMT
ARG SWIFT_VERSION=swift-6.2.4-RELEASE
# Fri, 27 Feb 2026 22:43:24 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 27 Feb 2026 22:43:24 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 27 Feb 2026 22:43:24 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:7b625f12eaf5f52ff71ffa6d83678b0481194ed88dfaa20ee4b8481abb9ba247`  
		Last Modified: Tue, 10 Feb 2026 18:14:19 GMT  
		Size: 64.8 MB (64799476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeca7a526ee6cee886d2dd12d08cb0598cc258430bc3a9253ee4530ce59689b`  
		Last Modified: Fri, 27 Feb 2026 22:43:53 GMT  
		Size: 198.4 MB (198443414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:c12262af1886d74c6268d0d05735e8831475c808cd0e3a3876c003aa037e6ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0da3b85ef8016ce09527b52775fafb86807d907c86d4f7838bf93385890de29`

```dockerfile
```

-	Layers:
	-	`sha256:755b8ec7fafb05a34f4eb7b20a3f5ff07dc1a792767052334d85f1aa8c335e76`  
		Last Modified: Fri, 27 Feb 2026 22:43:48 GMT  
		Size: 5.1 MB (5081631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4631a1d9880cbdc029c440b72c6fabbec03e589eae0c88cb047439f679634974`  
		Last Modified: Fri, 27 Feb 2026 22:43:48 GMT  
		Size: 11.9 KB (11946 bytes)  
		MIME: application/vnd.in-toto+json
