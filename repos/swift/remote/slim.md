## `swift:slim`

```console
$ docker pull swift@sha256:b696462831a6f37e0eecdbb4a6a9674eb866c376b17cb3c8479cdcec0cf27bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:slim` - linux; amd64

```console
$ docker pull swift@sha256:fb480046a67ee4f33779cd8ee9221bb24eb94400a9e1a16f314aaeb4a183a406
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131706573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a3e3b1359053470cec635e9d84f0b07efc4a8732a4c1580a616707d4bd8002`
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
# Fri, 02 Sep 2022 05:51:49 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libatomic1     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:51:49 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 02 Sep 2022 05:51:49 GMT
ARG SWIFT_PLATFORM=ubuntu18.04
# Fri, 02 Sep 2022 05:51:49 GMT
ARG SWIFT_BRANCH=swift-5.6.2-release
# Fri, 02 Sep 2022 05:51:49 GMT
ARG SWIFT_VERSION=swift-5.6.2-RELEASE
# Fri, 02 Sep 2022 05:51:49 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 02 Sep 2022 05:51:49 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu18.04 SWIFT_BRANCH=swift-5.6.2-release SWIFT_VERSION=swift-5.6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 02 Sep 2022 05:52:22 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b6021bb992daf8a0b959f468e6a19f21fe41d4f95cb650ac1d5369ff95f9d6`  
		Last Modified: Fri, 02 Sep 2022 06:18:50 GMT  
		Size: 20.5 MB (20479522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694eed3f430d2de863842f153d208a9803c6c15917f1e7c456f18875c8cb0b9a`  
		Last Modified: Fri, 02 Sep 2022 06:18:59 GMT  
		Size: 84.5 MB (84516966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
