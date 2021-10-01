## `swift:bionic`

```console
$ docker pull swift@sha256:ea2b66a9d4b5f035585535b05b8a520fc6aa9e2d0210baf77eaf6d46a4577e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:bionic` - linux; amd64

```console
$ docker pull swift@sha256:a59cc74a241f79280c3401fce46b985965ff4f740c6e64e2df744c7233ebaa2c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **743.6 MB (743593129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d08f2d35e133890e338da84611f0524eaa4e877dcd6616e36df0db81a0dbf9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:23 GMT
ADD file:0d82cd095966e8ee78b593cb47a352eec842edb7bd9d9468e8a70154522447d1 in / 
# Fri, 01 Oct 2021 02:23:24 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:43:13 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Fri, 01 Oct 2021 03:43:13 GMT
LABEL Description=Docker Container for the Swift programming language
# Fri, 01 Oct 2021 03:43:54 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libatomic1     libcurl4     libxml2     libedit2     libsqlite3-0     libc6-dev     binutils     libgcc-5-dev     libstdc++-5-dev     zlib1g-dev     libpython3.6     tzdata     git     pkg-config     && rm -r /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:43:55 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 01 Oct 2021 03:43:55 GMT
ARG SWIFT_PLATFORM=ubuntu18.04
# Fri, 01 Oct 2021 03:43:55 GMT
ARG SWIFT_BRANCH=swift-5.5-release
# Fri, 01 Oct 2021 03:43:56 GMT
ARG SWIFT_VERSION=swift-5.5-RELEASE
# Fri, 01 Oct 2021 03:43:56 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Fri, 01 Oct 2021 03:43:56 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu18.04 SWIFT_BRANCH=swift-5.5-release SWIFT_VERSION=swift-5.5-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Fri, 01 Oct 2021 03:45:55 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Fri, 01 Oct 2021 03:46:00 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:284055322776031bac33723839acb0db2d063a525ba4fa1fd268a831c7553b26`  
		Last Modified: Fri, 01 Oct 2021 02:25:02 GMT  
		Size: 26.7 MB (26705075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4048ed5a02d58ad597743ad2cc7c4730be97bd86db48271cf2496dae541b12`  
		Last Modified: Fri, 01 Oct 2021 04:30:27 GMT  
		Size: 124.7 MB (124703208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f839d163250d8a757c29de55a8c1f78b5fc84c655fd3e4e66ed3522f8f7695`  
		Last Modified: Fri, 01 Oct 2021 04:31:30 GMT  
		Size: 592.2 MB (592184618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d42685be5a08c74c2ca9b83284c92d85d1f7aa317175ff12411d1e8c28e1fe4`  
		Last Modified: Fri, 01 Oct 2021 04:30:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
