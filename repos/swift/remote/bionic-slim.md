## `swift:bionic-slim`

```console
$ docker pull swift@sha256:d11c9ea745a332d954a5ee23c72bfb5f3b4ca8c46e007b2594a7fc76356faafc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:bionic-slim` - linux; amd64

```console
$ docker pull swift@sha256:1aceb503e6c9774c87d430dbe645b96a01ad23a7ce1e162a999bb5b04d93e8f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.9 MB (129859502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960c123a504d4fefc01a97bb78e954e31decac2f616ad58732e155215a17d1bc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:53:37 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 01 Jun 2023 23:53:37 GMT
LABEL Description=Docker Container for the Swift programming language
# Thu, 01 Jun 2023 23:56:55 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libatomic1     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:56:55 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 01 Jun 2023 23:56:56 GMT
ARG SWIFT_PLATFORM=ubuntu18.04
# Thu, 01 Jun 2023 23:56:56 GMT
ARG SWIFT_BRANCH=swift-5.8-release
# Thu, 01 Jun 2023 23:56:56 GMT
ARG SWIFT_VERSION=swift-5.8-RELEASE
# Thu, 01 Jun 2023 23:56:56 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 01 Jun 2023 23:56:56 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu18.04 SWIFT_BRANCH=swift-5.8-release SWIFT_VERSION=swift-5.8-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 01 Jun 2023 23:57:25 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:41af1b5f0f51947706ae712999cf098bef968a7799e7cb4bb2268829e62a6ab3`  
		Last Modified: Fri, 02 Jun 2023 00:09:06 GMT  
		Size: 26.7 MB (26717357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1421a48301dad8fbf65b086c2b2868fc98050a04faadc34029accc3283eaaf`  
		Last Modified: Fri, 02 Jun 2023 00:21:38 GMT  
		Size: 20.5 MB (20479808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67df07230fb7456a52ebf3cb511b4c77e4080d44054e872cd733f010c02dda3`  
		Last Modified: Fri, 02 Jun 2023 00:21:46 GMT  
		Size: 82.7 MB (82662337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
