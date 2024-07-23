## `swift:fedora39`

```console
$ docker pull swift@sha256:085387509f443e0d77f7c9b96e5062e2dbdd221d1462cf2339f39f692ed4e701
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `swift:fedora39` - linux; amd64

```console
$ docker pull swift@sha256:5c25f0882aebd3a79b41a663a0c88e487745af9e089af50b4fcfc9a21955a301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1128086372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7ede3f6eac113b50b8a04f4a35948c7339a5ad889c9f5889e6923dc8b9bb41`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 06 Jun 2024 15:11:32 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Thu, 06 Jun 2024 15:11:32 GMT
ADD fedora-39-x86_64.tar.xz / # buildkit
# Thu, 06 Jun 2024 15:11:32 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 06 Jun 2024 15:11:32 GMT
RUN yum -y install   binutils   gcc   git   unzip   libcurl-devel   libedit-devel   libicu-devel   sqlite-devel   libuuid-devel   libxml2-devel   python3-devel # buildkit
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_PLATFORM=fedora39
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Jun 2024 15:11:32 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=fedora39 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Jun 2024 15:11:32 GMT
# ARGS: SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=fedora39 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Thu, 06 Jun 2024 15:11:32 GMT
# ARGS: SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=fedora39 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:f5752d20f619cb7038bc2c6944238eed3cd82936d6524e72ed7d35fff857f35c`  
		Last Modified: Tue, 23 Jul 2024 18:14:11 GMT  
		Size: 64.8 MB (64807226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245c1c31b507125cdefd56fdbab81d706099bed33f74a3f1935ae0c77ac95979`  
		Last Modified: Tue, 23 Jul 2024 19:15:03 GMT  
		Size: 342.6 MB (342586002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b118e171f98f1f49374e76002c2b09139462a7a236ef17bfed95be56699d6ad3`  
		Last Modified: Mon, 22 Jul 2024 22:11:00 GMT  
		Size: 720.7 MB (720692973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce30dfeaf01dbc0a58dd74f13ee004fecb27d02fb417a6c7652dbccbd8307de`  
		Last Modified: Tue, 23 Jul 2024 19:14:59 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:fedora39` - unknown; unknown

```console
$ docker pull swift@sha256:bb22cd4344c2b5639e1a9d95ebb6628846b2ea44a94ab9ef73494c503355c996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9397432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232ad48641377daa941679baee3ecb7b127c8a0a5f42b65f8bff860942bb9609`

```dockerfile
```

-	Layers:
	-	`sha256:0462a8663bd81bc8b75d92ebeeca22027c796218df4892a7f32372188709d5d2`  
		Last Modified: Tue, 23 Jul 2024 19:14:59 GMT  
		Size: 9.4 MB (9382886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14983f14c921e303cd85bb27ccfae53775e07a31979ba4f480086d5a6499a284`  
		Last Modified: Tue, 23 Jul 2024 19:14:59 GMT  
		Size: 14.5 KB (14546 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:fedora39` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:f356e3689aedadfbb23290fb79167878ab4673823b6f416b78dbc380d7b4e463
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1017343165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e51e6c67d2f6d89cd8f11da5978903bb092c5367b03182733a13a308335ada`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 19:58:13 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 13 Mar 2023 20:39:50 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Mon, 22 Apr 2024 17:40:07 GMT
ADD file:95cfb02bd93b25bcbe27281ad9d77e7f3351ade6bab85ce9b6160d74235b29a8 in / 
# Mon, 22 Apr 2024 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 07 Jun 2024 03:39:07 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 07 Jun 2024 03:39:07 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 07 Jun 2024 03:51:38 GMT
RUN yum -y install   binutils   gcc   git   unzip   libcurl-devel   libedit-devel   libicu-devel   sqlite-devel   libuuid-devel   libxml2-devel   python3-devel
# Fri, 07 Jun 2024 03:51:42 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 07 Jun 2024 03:51:42 GMT
ARG SWIFT_PLATFORM=fedora39
# Fri, 07 Jun 2024 03:51:42 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Fri, 07 Jun 2024 03:51:42 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Fri, 07 Jun 2024 03:51:43 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 07 Jun 2024 03:51:43 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=fedora39 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 07 Jun 2024 03:52:29 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Fri, 07 Jun 2024 03:52:42 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:22bb2152dc6386a1d2269ed00e37f29db25a6003edd92e1e785aace8b93f657c`  
		Last Modified: Mon, 22 Apr 2024 17:41:02 GMT  
		Size: 63.3 MB (63332208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7926c843cb485ace41c41024443ea353c591f1566a888364faf317827a1262c4`  
		Last Modified: Fri, 07 Jun 2024 04:08:18 GMT  
		Size: 336.6 MB (336565406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1ab81a3ed7dfcd9fd66cca45393ab864b1340282056308cc57a984a23bc0a2`  
		Last Modified: Fri, 07 Jun 2024 04:08:58 GMT  
		Size: 617.4 MB (617445375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d146c4108b2d367365676112e20d7e851adc078732196534575ec4905a6282e`  
		Last Modified: Fri, 07 Jun 2024 04:07:56 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
