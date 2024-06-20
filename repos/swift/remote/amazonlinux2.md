## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:0924efb57658ab1bc5d0494177b55ae113b42c67cfbb7b5a325255211773c511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:0a224bcf42daeb4247db420bd1f111a2d86b086f11c855e530af71bfd38a32f5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.5 MB (982537521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d5d4af948c8df068379d9410061357e4eb68b2586661b54ba7fc8194e0cb22a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Jun 2024 17:20:29 GMT
COPY dir:4184bb78726a0c9ceccafb2f51aa4c1f9147f3cd1379888561d889de0d9e48af in / 
# Thu, 20 Jun 2024 17:20:29 GMT
CMD ["/bin/bash"]
# Thu, 20 Jun 2024 18:27:36 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 20 Jun 2024 18:27:36 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 20 Jun 2024 18:28:09 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel
# Thu, 20 Jun 2024 18:28:12 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 20 Jun 2024 18:28:12 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Thu, 20 Jun 2024 18:28:12 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Thu, 20 Jun 2024 18:28:12 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Thu, 20 Jun 2024 18:28:12 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 20 Jun 2024 18:28:12 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 20 Jun 2024 18:29:05 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Thu, 20 Jun 2024 18:29:12 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:492439933c1ff7612b0a83687414326a9f2b12f1ab63e5ac2e42a257e9834145`  
		Last Modified: Thu, 13 Jun 2024 01:57:58 GMT  
		Size: 62.6 MB (62646452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015c52c4925ed23b7bae24867581d69db278bd6bd12535c59717afc99435036e`  
		Last Modified: Thu, 20 Jun 2024 18:45:31 GMT  
		Size: 295.2 MB (295226070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0554da0b0a26ebaf3f3a71f7e33f4c82b5e0071b34f13631811f7a7a980c3cdc`  
		Last Modified: Thu, 20 Jun 2024 18:46:21 GMT  
		Size: 624.7 MB (624664825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b73e72b4c03b17f131e5797cb143ea52c06a090564113f2a622854184dec6f`  
		Last Modified: Thu, 20 Jun 2024 18:44:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:c61686a51e99e52d1a8fac6a486a687abbd8f4b4d06f92aed0e96e62e73cb68d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **949.3 MB (949305575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d3bee652f288c7fa156a3597e170afc0d1ebd6ffe481306867a869f0038da6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Jun 2024 17:39:45 GMT
COPY dir:23934f7f3a9c4ad2c0f7afe64c708fe8194f94cafce3bfbba33d3cd60b2fc65e in / 
# Thu, 20 Jun 2024 17:39:47 GMT
CMD ["/bin/bash"]
# Thu, 20 Jun 2024 17:58:00 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 20 Jun 2024 17:58:00 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 20 Jun 2024 17:58:24 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel
# Thu, 20 Jun 2024 17:58:29 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 20 Jun 2024 17:58:29 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Thu, 20 Jun 2024 17:58:29 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Thu, 20 Jun 2024 17:58:30 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Thu, 20 Jun 2024 17:58:30 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 20 Jun 2024 17:58:30 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 20 Jun 2024 18:01:33 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Thu, 20 Jun 2024 18:01:46 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:6b964e874adca881e086a1062b2772882d2bcb2401e15ce21606f20d7a58e7de`  
		Last Modified: Thu, 13 Jun 2024 01:57:59 GMT  
		Size: 64.6 MB (64568709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4464a6957fe38a2a49fb56a6a7408efe209ae4bf80a95b82fd91ae8a1a5c0a3`  
		Last Modified: Thu, 20 Jun 2024 18:10:48 GMT  
		Size: 266.7 MB (266717554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfabebac7cf9c2ef38e54c5dd50a7a67d65aefa926d5f6afd17a1fa3fd77f3fe`  
		Last Modified: Thu, 20 Jun 2024 18:11:24 GMT  
		Size: 618.0 MB (618019137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c84d1417f867513b14d204dabd31d12c474e916440835a3cb4902bae5f13fb`  
		Last Modified: Thu, 20 Jun 2024 18:10:23 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
