## `swift:latest`

```console
$ docker pull swift@sha256:b241669961032655ad1890080a081c9f16555738dd6aae6f4f2698a8b25ac028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:latest` - linux; amd64

```console
$ docker pull swift@sha256:e33ba724d8c6acd6ec73c36a6b6027e2985069629485550a41b7559409dbc586
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.5 MB (704539751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1575f5e78aeaededc98f56f199d11b23e6984756b022cbb3dd7ae217b744ca`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:20:25 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 19 Mar 2022 21:20:25 GMT
LABEL Description=Docker Container for the Swift programming language
# Sat, 19 Mar 2022 21:22:15 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libatomic1     libcurl4-openssl-dev     libxml2-dev     libedit2     libsqlite3-0     libc6-dev     binutils     libgcc-5-dev     libstdc++-5-dev     zlib1g-dev     libpython3.6     tzdata     git     pkg-config     && rm -r /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:22:16 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Sat, 19 Mar 2022 21:22:16 GMT
ARG SWIFT_PLATFORM=ubuntu18.04
# Sat, 19 Mar 2022 21:22:16 GMT
ARG SWIFT_BRANCH=swift-5.6-release
# Sat, 19 Mar 2022 21:22:16 GMT
ARG SWIFT_VERSION=swift-5.6-RELEASE
# Sat, 19 Mar 2022 21:22:16 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 19 Mar 2022 21:22:16 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu18.04 SWIFT_BRANCH=swift-5.6-release SWIFT_VERSION=swift-5.6-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 19 Mar 2022 21:23:43 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Sat, 19 Mar 2022 21:23:47 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec91f2bd707b9601bcb3fec70a45b6d6bf9fa1c519290d761c2b1f6192b1af0`  
		Last Modified: Sat, 19 Mar 2022 22:03:13 GMT  
		Size: 151.7 MB (151721060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04208db4f5d961a63959f9d6ab5d738eef7e734409f7a1646d6f48f5498a524b`  
		Last Modified: Sat, 19 Mar 2022 22:04:03 GMT  
		Size: 526.1 MB (526109834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5181e354603539ebc7ab1b9eb2f4840c16d26ed8ac6b73d394541cec02f02033`  
		Last Modified: Sat, 19 Mar 2022 22:02:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
