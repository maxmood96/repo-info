## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:e75ccd79ac338d05a6f5c87e93ac305be4c96869ded4d6813b095b221fb02d59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:7dca9381c36f48384c4db22adde7f92dc10192a45f88ed7c1f426eabba0c790d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1634250814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44c4a289e7dd2890b98a3763adaa8ca41eb7b2580b6907928d8837160749041`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:59 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:59 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:17:25 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 22 Jun 2026 18:17:25 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 22 Jun 2026 18:17:25 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Mon, 22 Jun 2026 18:17:25 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 22 Jun 2026 18:17:25 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Mon, 22 Jun 2026 18:17:25 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Mon, 22 Jun 2026 18:17:25 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Mon, 22 Jun 2026 18:17:25 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 22 Jun 2026 18:17:25 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 22 Jun 2026 18:18:07 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Mon, 22 Jun 2026 18:18:08 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:b5a31d0a32c9342b5b53f098c4d8ac4fadeb6cbc6b34b2e4424fd39eb880bf9a`  
		Last Modified: Sat, 13 Jun 2026 04:09:34 GMT  
		Size: 62.9 MB (62942019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5773b0cac4e4d995e647f7eccd8ff71f598e536b265dcc7d0e3f1ad46050c487`  
		Last Modified: Mon, 22 Jun 2026 18:20:43 GMT  
		Size: 334.5 MB (334500104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b3211f73ed6dab4ae86b6305f4bd1df945dcc072033bbff38184751bac5da2`  
		Last Modified: Wed, 13 May 2026 18:21:34 GMT  
		Size: 1.2 GB (1236808518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f536e64a649d8ca1e0c1ba8d5382b0389c8535ec57d1211fdfac9eb4a9ccd3b3`  
		Last Modified: Mon, 22 Jun 2026 18:20:33 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:63cfd0b31ffad766beba4a8f95dc6af71db4da5a96ad9734a4daca19b09cd55b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12734941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac898a6d9f49017ff2781aaa8091a722ad60ab992635863d209443b12848085`

```dockerfile
```

-	Layers:
	-	`sha256:e6d5d63dab2702f19fa03634a222d236af465289811d40f164708fa3b441c733`  
		Last Modified: Mon, 22 Jun 2026 18:20:34 GMT  
		Size: 12.7 MB (12720094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5013468a5dd2fea5b67d873150e7f82c4e892f1cbc30460bc4d6a2f6f2783023`  
		Last Modified: Mon, 22 Jun 2026 18:20:33 GMT  
		Size: 14.8 KB (14847 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:67773f5badbc87d100ca2f79d2ed40d97181a59aa10d3bf5e1d3e95cf60c8d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1589962235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1592cf6e4d373800499635741cba3653ca924bb81c82281db6263419173f1725`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 18:00:28 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 18:00:28 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:15:55 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 22 Jun 2026 18:15:55 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 22 Jun 2026 18:15:55 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Mon, 22 Jun 2026 18:15:55 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 22 Jun 2026 18:15:55 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Mon, 22 Jun 2026 18:15:55 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Mon, 22 Jun 2026 18:15:55 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Mon, 22 Jun 2026 18:15:55 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 22 Jun 2026 18:15:55 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 22 Jun 2026 18:16:40 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Mon, 22 Jun 2026 18:16:40 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:4b30ecc040ec91b7e580ef7f93f591eaf80422b110a473c44b4d0dbcb2301395`  
		Last Modified: Wed, 17 Jun 2026 13:06:48 GMT  
		Size: 64.8 MB (64794736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bb843cdb983dbea7ec8a34c859ae1e3777f474829f45a71fc44b24d04638cf`  
		Last Modified: Mon, 22 Jun 2026 18:19:15 GMT  
		Size: 305.6 MB (305575746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d68a9c69fcab24bcd6f286aa786dddc8f06148d2d1aaa2897e551ec726f7608`  
		Last Modified: Wed, 13 May 2026 18:08:41 GMT  
		Size: 1.2 GB (1219591580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b2cc6415a321fe0b4f664270e4dfe07f93179635a8b7193ac3c14dc1bb9ecc`  
		Last Modified: Mon, 22 Jun 2026 18:19:09 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:4da7156db4129ef375a92fd59441073e13169370dec4e5872482d7ad77ffc925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12596700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923efa5f0854cf679715f3067af3e74c3970dc52b4aa2a91ee706b941132ffab`

```dockerfile
```

-	Layers:
	-	`sha256:edea44ac43234f056d1d3b3425674c07337a35e44f707e80f0314ec7eb8d2f64`  
		Last Modified: Mon, 22 Jun 2026 18:19:09 GMT  
		Size: 12.6 MB (12581731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b66a97f81b979e16e2eeda43b6e8bc23097b0a656bfb3182fab7498fb4aae645`  
		Last Modified: Mon, 22 Jun 2026 18:19:09 GMT  
		Size: 15.0 KB (14969 bytes)  
		MIME: application/vnd.in-toto+json
