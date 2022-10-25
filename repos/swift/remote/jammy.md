## `swift:jammy`

```console
$ docker pull swift@sha256:d42ad24385d26a34de539dec4ea044472d7049f013cb03b17dca9ec64de16e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:jammy` - linux; amd64

```console
$ docker pull swift@sha256:023ab3041c4187160dbda6bb6ec625f818abb658a9b75dec3332d0f2f80e7a78
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.9 MB (686880055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5ad9758d0fbc9d0412aad75c1c3ccf6119f16c5b57bfef209242b35d3a6853`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 18:32:36 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 25 Oct 2022 18:32:36 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 25 Oct 2022 18:34:03 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Tue, 25 Oct 2022 18:34:04 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Tue, 25 Oct 2022 18:34:04 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Tue, 25 Oct 2022 18:34:04 GMT
ARG SWIFT_BRANCH=swift-5.7-release
# Tue, 25 Oct 2022 18:34:04 GMT
ARG SWIFT_VERSION=swift-5.7-RELEASE
# Tue, 25 Oct 2022 18:34:04 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 25 Oct 2022 18:34:04 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.7-release SWIFT_VERSION=swift-5.7-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 25 Oct 2022 18:34:56 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Tue, 25 Oct 2022 18:35:03 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad40aeac95706db6e7a5aee2bd4694359900060fea1919580312a152be6626e`  
		Last Modified: Tue, 25 Oct 2022 19:12:12 GMT  
		Size: 103.5 MB (103473302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61575edfe2b17dc3a9db65620bd635642bc0a8e3a6d2138958bf56a53f01923d`  
		Last Modified: Tue, 25 Oct 2022 19:13:15 GMT  
		Size: 553.0 MB (552980143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71478fc0e8b07a930644e4de57d0e6b95524d45a57d1e0b639b36ce08b2dc901`  
		Last Modified: Tue, 25 Oct 2022 19:11:52 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:jammy` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:f8cf337d354f14becad4c9e641035ca22befe963b04e079a6813bea9b5683d22
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.1 MB (672078967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7b3eed4db815e6ab2c8112de938cec5125bfd2db8aff1a7d9e754d5e61bb9a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:06:28 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 05 Oct 2022 00:06:28 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 05 Oct 2022 00:06:59 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:07:00 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 05 Oct 2022 00:07:00 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Wed, 05 Oct 2022 00:07:01 GMT
ARG SWIFT_BRANCH=swift-5.7-release
# Wed, 05 Oct 2022 00:07:02 GMT
ARG SWIFT_VERSION=swift-5.7-RELEASE
# Wed, 05 Oct 2022 00:07:03 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 05 Oct 2022 00:07:04 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.7-release SWIFT_VERSION=swift-5.7-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 05 Oct 2022 00:07:46 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Wed, 05 Oct 2022 00:07:47 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ab52a3d3cb76167f361647c4a3acf25af6e2a7e8dac6e93b204c2a1261dac3`  
		Last Modified: Wed, 05 Oct 2022 00:15:05 GMT  
		Size: 100.6 MB (100632465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65d5e10cbec468d8bd82b6427580925a2951d8da925176b6a68fafc744caa8d`  
		Last Modified: Wed, 05 Oct 2022 00:16:04 GMT  
		Size: 543.1 MB (543064043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9525bb903e326e91acca92b6d71f1f971e98f58e97d650af74ed17d5ed243eeb`  
		Last Modified: Wed, 05 Oct 2022 00:14:49 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
