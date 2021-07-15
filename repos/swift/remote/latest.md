## `swift:latest`

```console
$ docker pull swift@sha256:afeaee88cf71f0f0b15ec3db504257abb63e78f6554e8f9091295dbf301424ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:latest` - linux; amd64

```console
$ docker pull swift@sha256:22eccf18158671fa4440b2643f5643094dafb9450f7769b9a05128d74aef9b95
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.5 MB (672453972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55144e60f95efab1aa0b5deda5901aec2bb3ad34839af65e1325abefb38e43ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 02:41:05 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Wed, 14 Jul 2021 02:41:05 GMT
LABEL Description=Docker Container for the Swift programming language
# Wed, 14 Jul 2021 02:43:10 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libatomic1     libcurl4     libxml2     libedit2     libsqlite3-0     libc6-dev     binutils     libgcc-5-dev     libstdc++-5-dev     zlib1g-dev     libpython3.6     tzdata     git     pkg-config     && rm -r /var/lib/apt/lists/*
# Wed, 14 Jul 2021 02:43:12 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 14 Jul 2021 02:43:12 GMT
ARG SWIFT_PLATFORM=ubuntu18.04
# Wed, 14 Jul 2021 02:43:12 GMT
ARG SWIFT_BRANCH=swift-5.4.2-release
# Wed, 14 Jul 2021 02:43:12 GMT
ARG SWIFT_VERSION=swift-5.4.2-RELEASE
# Wed, 14 Jul 2021 02:43:13 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Wed, 14 Jul 2021 02:43:13 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu18.04 SWIFT_BRANCH=swift-5.4.2-release SWIFT_VERSION=swift-5.4.2-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Wed, 14 Jul 2021 02:45:02 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver ha.pool.sks-keyservers.net --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Wed, 14 Jul 2021 02:45:07 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53185c7ef0326fe4500b46f91ea70118cbdef64ed60ac04abcea8ca6212aa0ea`  
		Last Modified: Wed, 14 Jul 2021 03:16:33 GMT  
		Size: 124.7 MB (124694998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4906d3fbd8eecca144a8d0f86b614781b4e739c9f959d6f2e23fc3606ae6db44`  
		Last Modified: Wed, 14 Jul 2021 03:17:29 GMT  
		Size: 521.1 MB (521052829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
