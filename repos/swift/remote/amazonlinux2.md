## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:ccf11729bf64fc33e544e6390fb0863482c8e3bcb1595f8ed387133e85636cb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:f82b3afbd6357554bec7d61b207114c5f7de7ac7022151466825ebc1e4057847
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **863.8 MB (863795190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:051b1d9602d24b91125629af0e75cfe7ac8902e0e919a027792f9c2e399f70ca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 May 2022 23:19:31 GMT
ADD file:386c34c6960464ef8f88891333fb091aef731602a28a185a9d6db27726fbe504 in / 
# Tue, 03 May 2022 23:19:32 GMT
CMD ["/bin/bash"]
# Tue, 03 May 2022 23:37:12 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 03 May 2022 23:37:12 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 03 May 2022 23:37:43 GMT
RUN yum -y install   binutils   gcc   git   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Tue, 03 May 2022 23:37:45 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Tue, 03 May 2022 23:37:46 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 03 May 2022 23:37:46 GMT
ARG SWIFT_BRANCH=swift-5.6.1-release
# Tue, 03 May 2022 23:37:46 GMT
ARG SWIFT_VERSION=swift-5.6.1-RELEASE
# Tue, 03 May 2022 23:37:46 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 03 May 2022 23:37:46 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.6.1-release SWIFT_VERSION=swift-5.6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 03 May 2022 23:38:21 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Tue, 03 May 2022 23:38:27 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:8de5b65bd171294b1e04e0df439f4ea11ce923b642eddf3b3d76d297bfd2670c`  
		Last Modified: Mon, 02 May 2022 22:06:03 GMT  
		Size: 62.3 MB (62291142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b05a763093ceb4185f94a25a8b1389b90f1434e14840c13333bb20b01bab52`  
		Last Modified: Tue, 03 May 2022 23:52:20 GMT  
		Size: 276.5 MB (276544190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9720c892fbb4f7a846855f1ff671551496fbcbb11b0050ac9b7c7f8758859c8`  
		Last Modified: Tue, 03 May 2022 23:53:05 GMT  
		Size: 525.0 MB (524959629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac8306ae7ceed26d56c52bc38308d66aa09f68775f95cc66935b626d9c0355b`  
		Last Modified: Tue, 03 May 2022 23:51:49 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:67b4fbb133165aa7681dd6ce17445d7a89e843fdbfccdfaf3a9efa253cb82eee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **805.5 MB (805526779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123026e68f2890bb4541871c940d94031e5b076bf7480bbe569f56c34f54c81a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 May 2022 22:39:32 GMT
ADD file:c351a8c80719ef38e02c26849f50bb7d79c24a6347cc2a72ae1a0768964bd113 in / 
# Tue, 03 May 2022 22:39:34 GMT
CMD ["/bin/bash"]
# Wed, 04 May 2022 00:17:06 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 04 May 2022 00:17:07 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 04 May 2022 00:17:30 GMT
RUN yum -y install   binutils   gcc   git   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Wed, 04 May 2022 00:17:31 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 04 May 2022 00:17:32 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Wed, 04 May 2022 00:17:33 GMT
ARG SWIFT_BRANCH=swift-5.6.1-release
# Wed, 04 May 2022 00:17:34 GMT
ARG SWIFT_VERSION=swift-5.6.1-RELEASE
# Wed, 04 May 2022 00:17:35 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 04 May 2022 00:17:36 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.6.1-release SWIFT_VERSION=swift-5.6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 04 May 2022 00:18:08 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Wed, 04 May 2022 00:18:10 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:ec3b4c26678b188d3874bed5e14dd278311fc05c81e418d5f0da36ec38d9f488`  
		Last Modified: Tue, 03 May 2022 03:07:52 GMT  
		Size: 63.9 MB (63902179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341f66977494846497ca2dbade335ac25fd789bf8d0d724b1f19bb5b7468bf2e`  
		Last Modified: Wed, 04 May 2022 00:19:58 GMT  
		Size: 236.5 MB (236455111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7100cbc77c7c2ae0277f830d6b177332fa37a9fb96067f6d6939c4101883b4a6`  
		Last Modified: Mon, 11 Apr 2022 20:39:46 GMT  
		Size: 505.2 MB (505169287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdb08550c4bc899db822d112db924bab3668977a155ab2e3a2afbec6374ec35`  
		Last Modified: Wed, 04 May 2022 00:19:30 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
