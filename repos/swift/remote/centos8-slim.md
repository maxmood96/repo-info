## `swift:centos8-slim`

```console
$ docker pull swift@sha256:fac3197524950163b816a521d0e0fc056b6ea6ed13be9a6b374a2b6892c554ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:centos8-slim` - linux; amd64

```console
$ docker pull swift@sha256:3f3882b2b2e8c5ad084fc28e63ead051cc545803cde69e0aebaaf975b81bb644
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114577930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc85c7bedf9c58ffaf4beff7a40985b81091d26c841be960b7dd89633ec813fd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 14:05:12 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Fri, 26 Mar 2021 14:05:13 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 26 Mar 2021 14:07:23 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 26 Mar 2021 14:07:23 GMT
ARG SWIFT_PLATFORM=centos8
# Mon, 13 Sep 2021 18:49:16 GMT
ARG SWIFT_BRANCH=swift-5.4.3-release
# Mon, 13 Sep 2021 18:49:16 GMT
ARG SWIFT_VERSION=swift-5.4.3-RELEASE
# Mon, 13 Sep 2021 18:49:16 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Mon, 13 Sep 2021 18:49:17 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=centos8 SWIFT_BRANCH=swift-5.4.3-release SWIFT_VERSION=swift-5.4.3-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Mon, 13 Sep 2021 18:50:34 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35d9127e21967e319c053bc84886faded727ba29801a3e9f5f15a16ffacecb7`  
		Last Modified: Mon, 13 Sep 2021 19:12:22 GMT  
		Size: 39.4 MB (39395931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
