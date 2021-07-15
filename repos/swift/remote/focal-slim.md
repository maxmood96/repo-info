## `swift:focal-slim`

```console
$ docker pull swift@sha256:c30c44e2ffa8644d0b3e98b88c093a9e40fedd6336c19481d5949775b09b794b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:focal-slim` - linux; amd64

```console
$ docker pull swift@sha256:424d8c0baa6d2065799acae4394dec1acec49ec8c2f81d1584527a8b767c8eb2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.4 MB (90350082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099431a8843fe92c335493ff2e87b1804c404fff1e33870acb0edfb946b731aa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 02:47:34 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Wed, 14 Jul 2021 02:47:35 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 14 Jul 2021 02:47:50 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Wed, 14 Jul 2021 02:47:51 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 14 Jul 2021 02:47:51 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Wed, 14 Jul 2021 02:47:51 GMT
ARG SWIFT_BRANCH=swift-5.4.2-release
# Wed, 14 Jul 2021 02:47:51 GMT
ARG SWIFT_VERSION=swift-5.4.2-RELEASE
# Wed, 14 Jul 2021 02:47:52 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Wed, 14 Jul 2021 02:47:52 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.4.2-release SWIFT_VERSION=swift-5.4.2-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Wed, 14 Jul 2021 02:49:22 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver ha.pool.sks-keyservers.net --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ddc2ded38cc318d32299996222e8bd02fc9ba5695e80355d3bcdebc364d8e8`  
		Last Modified: Wed, 14 Jul 2021 03:18:24 GMT  
		Size: 22.3 MB (22250747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d4eba6df753a13519236495db90146948bdc0f3ddf9a4d67d0db24b9394fc2`  
		Last Modified: Wed, 14 Jul 2021 03:18:27 GMT  
		Size: 39.5 MB (39533472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
