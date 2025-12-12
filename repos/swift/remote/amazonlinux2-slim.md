## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:69d1ba26bf25ef8f378070e74bd48b7a0c28b78dd1dcf6e96d76843c1e1edac9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:87e5bd5e07f82b117c710f7ebdddc3c8555ee99cb9b0909a809ab33dc8a4d784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284374898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2888408ade818fc83e878266a259ccd1c098b18f51eadca20ed4b65d3ae92736`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:30 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:30 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:13:54 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 11 Dec 2025 22:13:54 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 11 Dec 2025 22:13:54 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 11 Dec 2025 22:13:54 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Thu, 11 Dec 2025 22:13:54 GMT
ARG SWIFT_BRANCH=swift-6.2.2-release
# Thu, 11 Dec 2025 22:13:54 GMT
ARG SWIFT_VERSION=swift-6.2.2-RELEASE
# Thu, 11 Dec 2025 22:13:54 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 11 Dec 2025 22:13:54 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 11 Dec 2025 22:13:54 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:364e8e668f0e62a54627e7d364c5d2a3a16f70f1c962628fd84b9ef8fb667d21`  
		Last Modified: Thu, 11 Dec 2025 05:04:46 GMT  
		Size: 62.9 MB (62940975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005bd098507526c0f1267932b97f33d8d7619a717b7c6004b25a666481672236`  
		Last Modified: Thu, 11 Dec 2025 22:14:35 GMT  
		Size: 221.4 MB (221433923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:97a29c8efe08fc55ecffe6935fb72c629325f0c11bfb0ee63edad7cce386b424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c29d17013f281248b997e572e201a23e1951776973291aa041603c2881ccd4d`

```dockerfile
```

-	Layers:
	-	`sha256:129f56ef1d8c8d6b24c46150c7a795ec8bd045d3c87e8369b3695d13a9a760e3`  
		Last Modified: Thu, 11 Dec 2025 23:48:49 GMT  
		Size: 5.1 MB (5082197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1940b077ab8fbc054a1b546b41f29f186aa7f7958b8da5d80d162f4cbe3f7fba`  
		Last Modified: Thu, 11 Dec 2025 23:48:50 GMT  
		Size: 11.9 KB (11854 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:a9e12340276685d4539611b00ad2e2ae9f33c65eb72ef2732e3e153f6dec0bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.7 MB (261728248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df25231a1f5332628be8ba5ad7aa495276395627a5b2e362a6cffa4d78a4103`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:28 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:28 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:13:33 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 11 Dec 2025 22:13:33 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 11 Dec 2025 22:13:33 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 11 Dec 2025 22:13:33 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Thu, 11 Dec 2025 22:13:33 GMT
ARG SWIFT_BRANCH=swift-6.2.2-release
# Thu, 11 Dec 2025 22:13:33 GMT
ARG SWIFT_VERSION=swift-6.2.2-RELEASE
# Thu, 11 Dec 2025 22:13:33 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 11 Dec 2025 22:13:33 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 11 Dec 2025 22:13:33 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3025a603ec7f965108d80dc4fec89e78b51f11053fd1c2315d47a1be11fbe2`  
		Last Modified: Thu, 11 Dec 2025 22:20:27 GMT  
		Size: 196.9 MB (196932493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:ad3c701ce96b61bc64195fee69336203695259d5dd2acd42e43468635c3ebd30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf74fda97a530a7e40f06a6287455e016883bbc4d1f237e4d5d563aca3ff86a`

```dockerfile
```

-	Layers:
	-	`sha256:fa35cae2c0890a1f2f45c867a47e1686fdcd91b74a53703a217d135c60122958`  
		Last Modified: Thu, 11 Dec 2025 23:48:55 GMT  
		Size: 5.1 MB (5081631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7455d687273ddecd9762ec40b21b1dc0e555a823a1d317774549a439a9bb501`  
		Last Modified: Thu, 11 Dec 2025 23:48:56 GMT  
		Size: 11.9 KB (11946 bytes)  
		MIME: application/vnd.in-toto+json
