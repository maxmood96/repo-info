## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:ca0f9cadc108efff32e32e0f89c41f6b8476670f1f65d17a8c98e1657504ec3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:1e605e5adb6fe5eb3ea519f81b7e27ce3aee199674238d9ebf23f14bd969e13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.1 MB (267084874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3079ce3853e38692ad7bfa69c90b1e7c9208b38eab2d60293e3068540245de4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Dec 2024 07:44:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 12 Dec 2024 07:44:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_BRANCH=swift-6.0.3-release
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_VERSION=swift-6.0.3-RELEASE
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:f3dc83dc2e4e000fd189efee126db80e38a079b47b8e5229a794a0a6148bfec6`  
		Last Modified: Sat, 08 Mar 2025 04:13:59 GMT  
		Size: 62.8 MB (62772838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f913e615abfb714937d67401576040f8242ca3797ba023b3aa8f9548cb719380`  
		Last Modified: Thu, 13 Mar 2025 22:53:59 GMT  
		Size: 204.3 MB (204312036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:e7c84df955110a498c36f3cafc00faea827b4f89f3fe0b3b0b46b3b443fcae1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5079441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62cb36ebe2655539e9418589254613eff009dace0b647dcc5bc129a7e4e1c6c8`

```dockerfile
```

-	Layers:
	-	`sha256:f67cb138fd7f9c72e020b236c59b91ad2fdaf990106c1a428e73cc4596946bbb`  
		Last Modified: Thu, 13 Mar 2025 22:53:56 GMT  
		Size: 5.1 MB (5067544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dfe3983d5744f27c1be746b18ca26bb0e3513cb950580f2a94e03a4e9939d11`  
		Last Modified: Thu, 13 Mar 2025 22:53:56 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:74071b81a6d5e2446fa3bbf340c2af859e2c6ca21560c355175017452c345d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244531523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddadba5dafe9ebe9c4fd9766aa2f38fc022eec592753d856babe15d9a8b1e616`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Dec 2024 07:44:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 12 Dec 2024 07:44:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_BRANCH=swift-6.0.3-release
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_VERSION=swift-6.0.3-RELEASE
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:37d03ccf62e80c78860df81fce0c2ae4e2349efe1a11714ff404080836c55d45`  
		Last Modified: Mon, 10 Mar 2025 14:33:01 GMT  
		Size: 64.6 MB (64576854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b20a5ac12292c8fc771c045713a1931d9d2cd7a6f50f1630c9f00a659768376`  
		Last Modified: Fri, 14 Mar 2025 00:27:51 GMT  
		Size: 180.0 MB (179954669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:cec74609cac12639dbe043ca90b4d6084ff0257e84ea8eff0848be3a2abc7572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5078966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799716a2d047a648f50f44fcc3fd3a7d557f17e15e0088d031456e24ed95764f`

```dockerfile
```

-	Layers:
	-	`sha256:a708efd237e60b2819fb7ba0a3151ab61cc3bab9ce01f0bf5375ec02225c1e7d`  
		Last Modified: Fri, 14 Mar 2025 00:27:47 GMT  
		Size: 5.1 MB (5066978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e1e11414174b69b519cbd8b87a2cb1514c68d5e88c826b60cf3521e52afe26d`  
		Last Modified: Fri, 14 Mar 2025 00:27:47 GMT  
		Size: 12.0 KB (11988 bytes)  
		MIME: application/vnd.in-toto+json
