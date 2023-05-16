## `swift:bionic-slim`

```console
$ docker pull swift@sha256:60b3cf1adb16ff77a456b062e83510b786456d1fbec5bd2781a28df6f2a863a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:bionic-slim` - linux; amd64

```console
$ docker pull swift@sha256:461e1401ff0c22e6ed95391b099ec6332bdd97815ae19e2895c9eae806e42063
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129848677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdbbffdd51be1af62a290174f63666ce39a28bfbc36dde45ffe6a446d1c5dddc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 May 2023 09:41:51 GMT
ARG RELEASE
# Fri, 12 May 2023 09:41:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 May 2023 09:41:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 May 2023 09:41:51 GMT
LABEL org.opencontainers.image.version=18.04
# Fri, 12 May 2023 09:41:52 GMT
ADD file:47682dd3869ca8e57ceb15f69a6ac7c9048d4d42c7a99a976e597cf072423c12 in / 
# Fri, 12 May 2023 09:41:53 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 01:38:34 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 16 May 2023 01:38:34 GMT
LABEL Description=Docker Container for the Swift programming language
# Tue, 16 May 2023 01:40:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libatomic1     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Tue, 16 May 2023 01:40:22 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Tue, 16 May 2023 01:40:22 GMT
ARG SWIFT_PLATFORM=ubuntu18.04
# Tue, 16 May 2023 01:40:22 GMT
ARG SWIFT_BRANCH=swift-5.8-release
# Tue, 16 May 2023 01:40:22 GMT
ARG SWIFT_VERSION=swift-5.8-RELEASE
# Tue, 16 May 2023 01:40:22 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 16 May 2023 01:40:22 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu18.04 SWIFT_BRANCH=swift-5.8-release SWIFT_VERSION=swift-5.8-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 16 May 2023 01:40:52 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:c67806d7e72dd941e600bad2eabe920a17ba1852b325b63900c819ffeae646fb`  
		Last Modified: Tue, 16 May 2023 01:01:48 GMT  
		Size: 26.7 MB (26715509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8060c6645dd5a1f1a4a5d280be008a866f3209841c52c413439897c1526d586a`  
		Last Modified: Tue, 16 May 2023 01:58:40 GMT  
		Size: 20.5 MB (20470733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a579efef566ca25cc9c412bb71c6435d0bc48c20efc27144ba85dbb6be2bcf`  
		Last Modified: Tue, 16 May 2023 01:58:49 GMT  
		Size: 82.7 MB (82662435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
