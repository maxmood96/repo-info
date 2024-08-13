## `swift:bookworm`

```console
$ docker pull swift@sha256:1c791e7d5e01af2cf020f3f69e10d90182d47ba60eee07baf4762ca715cbf635
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm` - linux; amd64

```console
$ docker pull swift@sha256:3ee682b3756ccafd65797cdf1155f98a6a37224866a456852605be24c94588db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **963.5 MB (963465653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f3f7d8d43d8ef979538f716bc0f48534ac9a436fbac2426433659a66846962`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 06 Jun 2024 15:11:32 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Thu, 06 Jun 2024 15:11:32 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 06 Jun 2024 15:11:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils-gold     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     && rm -r /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_PLATFORM=debian12
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Jun 2024 15:11:32 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Jun 2024 15:11:32 GMT
# ARGS: SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Thu, 06 Jun 2024 15:11:32 GMT
# ARGS: SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f4bcea28a5f5f0da7b5d24eaeed21692518d9a5cab82132b587be5db925e7d`  
		Last Modified: Tue, 13 Aug 2024 01:26:07 GMT  
		Size: 194.6 MB (194588660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28f2c206842c82eed24996dec139968c3e752d1ff7fc2a409ad9c3b35215c4d`  
		Last Modified: Tue, 13 Aug 2024 01:26:15 GMT  
		Size: 719.3 MB (719322738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88a4bb50fbdc05f77751a02ada1207e5c140c91d5314af3bfeba1bd914d7dd6`  
		Last Modified: Tue, 13 Aug 2024 01:26:05 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:09a00ed1a32ecb89a119d8ad7eb4c343b9acc1401f514804a937a6d2ded2f14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10449076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e45bda7c406db9a30e505a30cc19ca10a172a5dabb9115faf16d0f34908cd6c`

```dockerfile
```

-	Layers:
	-	`sha256:87a4716af03d889f3f3d5668d434f40d001f6811f4ea788df68a8cc5ff573826`  
		Last Modified: Tue, 13 Aug 2024 01:26:05 GMT  
		Size: 10.4 MB (10433585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7013d4640c65609e6c8f54838d5ed392b54cdfd1e5b9bb8d2dda2f15d76c6694`  
		Last Modified: Tue, 13 Aug 2024 01:26:05 GMT  
		Size: 15.5 KB (15491 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:bookworm` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:ed813627ff9d11d2205da17438fbc61567530d1fb159c2643e0c40b1984e3558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.9 MB (852850822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b04495c4b27da1e1e9d44cc9da85138447c66f850e0253043244a92939003e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 06 Jun 2024 15:11:32 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Thu, 06 Jun 2024 15:11:32 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 06 Jun 2024 15:11:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils-gold     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     && rm -r /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_PLATFORM=debian12
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Jun 2024 15:11:32 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Jun 2024 15:11:32 GMT
# ARGS: SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Thu, 06 Jun 2024 15:11:32 GMT
# ARGS: SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5475caaf56037cc163ef8d3a0a01a35b57cacd3f08d2244a13d4c6893532097c`  
		Last Modified: Tue, 13 Aug 2024 11:51:28 GMT  
		Size: 186.3 MB (186272747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63472accb5b96cbd97394a6fa22acaa249a0f3b97b64bcdce9366b72509cc64`  
		Last Modified: Tue, 13 Aug 2024 11:51:39 GMT  
		Size: 617.0 MB (616989309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4c350c32eac576b270dd7c95e5421c38def5f6f0ead4224e8ac36a2063e8ed`  
		Last Modified: Tue, 13 Aug 2024 11:51:23 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:27ea0edb18fbb1763b705c46cb1013372eac198ca340dbaf674d48775b506163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10477371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0971fa00e1d6db5b62a88367d1addc9ec9a2f93b45224d80e5262aa20e6e3de`

```dockerfile
```

-	Layers:
	-	`sha256:239314b86d565270b7271f54d31a3da384de32544843162eeab253e8070913c9`  
		Last Modified: Tue, 13 Aug 2024 11:51:24 GMT  
		Size: 10.5 MB (10461594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fabe0b260b2e1a8418ebc295578923d000464bb27505e5147521972813def60`  
		Last Modified: Tue, 13 Aug 2024 11:51:23 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json
