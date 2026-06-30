## `swift:amazonlinux2023`

```console
$ docker pull swift@sha256:f8b6b0d03e326cec3cf33ba2c1331c17ccf0fa260e3690b7c7f155304f680a1d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2023` - linux; amd64

```console
$ docker pull swift@sha256:bd46b38975a6f6df24802c9ade834df43af396996ff15e81839eab8a15d3c97e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1480144388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0868fa92b21b392c9c6a58d8098ac891fccb99231bac07ca0e3ba53891092a51`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:34 GMT
CMD ["/bin/bash"]
# Tue, 30 Jun 2026 18:56:54 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 30 Jun 2026 18:56:54 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 30 Jun 2026 18:56:54 GMT
RUN dnf -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata # buildkit
# Tue, 30 Jun 2026 18:56:57 GMT
RUN dnf -y swap gnupg2-minimal gnupg2-full # buildkit
# Tue, 30 Jun 2026 18:56:57 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 30 Jun 2026 18:56:57 GMT
ARG SWIFT_PLATFORM=amazonlinux2023
# Tue, 30 Jun 2026 18:56:57 GMT
ARG SWIFT_BRANCH=swift-6.3.3-release
# Tue, 30 Jun 2026 18:56:57 GMT
ARG SWIFT_VERSION=swift-6.3.3-RELEASE
# Tue, 30 Jun 2026 18:56:57 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 30 Jun 2026 18:56:57 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 30 Jun 2026 18:57:33 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Tue, 30 Jun 2026 18:57:34 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:43a4ccfcda545d0357b8595db01c68db022db4283c68d08e06427e6c91ac7063`  
		Last Modified: Sat, 13 Jun 2026 02:07:52 GMT  
		Size: 54.6 MB (54574183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bea8ec112520c7b044b39333448c49076843ff8baafd81df7a31bdc7a95634`  
		Last Modified: Tue, 30 Jun 2026 19:00:16 GMT  
		Size: 282.0 MB (281998124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbd781ecbfba4458e46e95cdab48ee8a8715671fa05499db454952d85ea0594`  
		Last Modified: Tue, 30 Jun 2026 19:00:04 GMT  
		Size: 24.2 MB (24160292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3e8ff26215c189d4f2b684f1a0c882440fed3ffd5c7427b175bce473dc304f`  
		Last Modified: Tue, 30 Jun 2026 19:00:36 GMT  
		Size: 1.1 GB (1119411616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf1752f9a1424c2da9b9493f92486bfbbd1831e55f36ce22eacb05aa8012c73`  
		Last Modified: Tue, 30 Jun 2026 19:00:02 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2023` - unknown; unknown

```console
$ docker pull swift@sha256:6b1f72fb1ac5ba4127cd7a3869cd2ad5de9114cdb360fba034e54f7db5e785e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13813311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9c31bed3c1ceddcd03dc8a0467f76e5ab18709a6e6835247e1f084bbd3fa7f`

```dockerfile
```

-	Layers:
	-	`sha256:662abba20773cee7081d35be2ced305f80c30b8d2184492a236742d670d2cbbf`  
		Last Modified: Tue, 30 Jun 2026 19:00:03 GMT  
		Size: 13.8 MB (13797084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba0bf9dbd807164d6f5080d2e3b46d0f3866ecda5604143c039cb1c627f249a8`  
		Last Modified: Tue, 30 Jun 2026 19:00:01 GMT  
		Size: 16.2 KB (16227 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2023` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:59296b802747c4ec978284d2e905a3ecf31f628ccc8b77d485e8e736932e4d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1461968104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e31fddad99d3d2657137e094f24b43de8d992ca8c95a5299a4e21b2232e399`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:55 GMT
CMD ["/bin/bash"]
# Tue, 30 Jun 2026 18:56:39 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 30 Jun 2026 18:56:39 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 30 Jun 2026 18:56:39 GMT
RUN dnf -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata # buildkit
# Tue, 30 Jun 2026 18:56:42 GMT
RUN dnf -y swap gnupg2-minimal gnupg2-full # buildkit
# Tue, 30 Jun 2026 18:56:42 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 30 Jun 2026 18:56:42 GMT
ARG SWIFT_PLATFORM=amazonlinux2023
# Tue, 30 Jun 2026 18:56:42 GMT
ARG SWIFT_BRANCH=swift-6.3.3-release
# Tue, 30 Jun 2026 18:56:42 GMT
ARG SWIFT_VERSION=swift-6.3.3-RELEASE
# Tue, 30 Jun 2026 18:56:42 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 30 Jun 2026 18:56:42 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 30 Jun 2026 18:57:26 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Tue, 30 Jun 2026 18:57:26 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:9d73cc96eee98f0257861d2c8c5e7eac1d4fd5e92dd1ed16608b0040908eb5e0`  
		Last Modified: Fri, 12 Jun 2026 22:22:20 GMT  
		Size: 53.5 MB (53450686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f904ed5fab7e0a0916602d54c4f9646d8ab0eb50153fe5c39bf39e669b684019`  
		Last Modified: Tue, 30 Jun 2026 18:59:56 GMT  
		Size: 273.3 MB (273319479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace75882ee72e28afb70dc9edaca8c1a63fbda52fada08ff8cda5ef5e73ceb79`  
		Last Modified: Tue, 30 Jun 2026 18:59:47 GMT  
		Size: 23.7 MB (23748925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c501b0b9e3b07cb98c1c4c814abf286c49cd43b3b040a59432e454bfeaec6f47`  
		Last Modified: Tue, 30 Jun 2026 19:00:19 GMT  
		Size: 1.1 GB (1111448842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78f05a5d6ddb7e138bb841e85bc259abf9c175067417836eadc38fd56b0ea64`  
		Last Modified: Tue, 30 Jun 2026 18:59:45 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2023` - unknown; unknown

```console
$ docker pull swift@sha256:802decd5436ef539359ad2ad9f4596358e074b9b764151711d4dd5ebe1f4440e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13683501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59399be879d064b3574ab23d9ac87ea520d18a91427ebb59fabd2e99e3013fc1`

```dockerfile
```

-	Layers:
	-	`sha256:14a1d9def7343a912ea4a411a9b0e4ee758c42cadeb1eb5e01c826b76c355253`  
		Last Modified: Tue, 30 Jun 2026 18:59:46 GMT  
		Size: 13.7 MB (13667137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1846463e65541e08c4f991b9e5cabb6e882cdccd0dbd1ab7f28dacdbc608c0b4`  
		Last Modified: Tue, 30 Jun 2026 18:59:45 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json
