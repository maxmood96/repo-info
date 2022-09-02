## `swift:bionic`

```console
$ docker pull swift@sha256:21004cd7b4e632d3e4550f06744f69650dd69cbe2cd801dd1204a517d94c2aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:bionic` - linux; amd64

```console
$ docker pull swift@sha256:b04f1ee428354c01ff5986cfc790d253c32a1aa5937d7d80653bd358520f5627
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.5 MB (704537719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caffe87adcfca651294bc0f90cec795d85ac3edf7b2dfd8e4a98ad440ea67cf5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:48:30 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 02 Sep 2022 05:48:30 GMT
LABEL Description=Docker Container for the Swift programming language
# Fri, 02 Sep 2022 05:50:42 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libatomic1     libcurl4-openssl-dev     libxml2-dev     libedit2     libsqlite3-0     libc6-dev     binutils     libgcc-5-dev     libstdc++-5-dev     zlib1g-dev     libpython3.6     tzdata     git     pkg-config     && rm -r /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:50:43 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 02 Sep 2022 05:50:43 GMT
ARG SWIFT_PLATFORM=ubuntu18.04
# Fri, 02 Sep 2022 05:50:44 GMT
ARG SWIFT_BRANCH=swift-5.6.2-release
# Fri, 02 Sep 2022 05:50:44 GMT
ARG SWIFT_VERSION=swift-5.6.2-RELEASE
# Fri, 02 Sep 2022 05:50:44 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 02 Sep 2022 05:50:44 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu18.04 SWIFT_BRANCH=swift-5.6.2-release SWIFT_VERSION=swift-5.6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 02 Sep 2022 05:51:26 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Fri, 02 Sep 2022 05:51:32 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320e8c4bf9dfd883fcc629faca0c3d80be42d31a5486abb38d5b955d43d0e5c4`  
		Last Modified: Fri, 02 Sep 2022 06:17:39 GMT  
		Size: 151.7 MB (151720022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256ecb5a94957096bf5b5298174d91e8dbe184474bfd253f5f683960807e42d1`  
		Last Modified: Fri, 02 Sep 2022 06:18:28 GMT  
		Size: 526.1 MB (526107382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479f4b0a8ffc6330badf27285bc22323ec49d5a6fd648f3579d3b8545f76cae8`  
		Last Modified: Fri, 02 Sep 2022 06:17:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
