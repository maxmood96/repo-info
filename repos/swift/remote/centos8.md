## `swift:centos8`

```console
$ docker pull swift@sha256:102ae4c07d36538b0a0897480b4201b972cd9cb6ad3aa311a4d5b87bb5e28094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `swift:centos8` - linux; amd64

```console
$ docker pull swift@sha256:48b17e6c90f374b5dceb88b20fe4eda9853475b54285bd5d5af5f08c415c0718
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.9 MB (671868343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04902644f69bbd458faae0a6189fbb6ef31c0cece1e120708eccc7870cc2e58`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Tue, 08 Dec 2020 00:59:20 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Tue, 08 Dec 2020 00:59:20 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 17 Dec 2020 16:30:14 GMT
RUN yum install -y https://dl.fedoraproject.org/pub/epel/epel-release-latest-8.noarch.rpm
# Thu, 17 Dec 2020 16:31:00 GMT
RUN yum install --enablerepo=powertools -y   binutils   gcc   git   glibc-static   libbsd-devel   libedit   libedit-devel   libicu-devel   libstdc++-static   pkg-config   python2   sqlite   zlib-devel
# Thu, 17 Dec 2020 16:31:02 GMT
RUN ln -s /usr/bin/python2 /usr/bin/python
# Thu, 17 Dec 2020 16:31:02 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 17 Dec 2020 16:31:02 GMT
ARG SWIFT_PLATFORM=centos8
# Thu, 17 Dec 2020 16:31:03 GMT
ARG SWIFT_BRANCH=swift-5.3.2-release
# Thu, 17 Dec 2020 16:31:03 GMT
ARG SWIFT_VERSION=swift-5.3.2-RELEASE
# Thu, 17 Dec 2020 16:31:04 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Thu, 17 Dec 2020 16:31:04 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=centos8 SWIFT_BRANCH=swift-5.3.2-release SWIFT_VERSION=swift-5.3.2-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Thu, 17 Dec 2020 16:32:27 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver ha.pool.sks-keyservers.net --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Thu, 17 Dec 2020 16:32:29 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a09423bc819f142f3bec7c84a18a00d3549f9dfc8358c933c274d29cb2dacc`  
		Last Modified: Thu, 17 Dec 2020 16:49:50 GMT  
		Size: 19.5 MB (19490910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e086faef87c7ea0badb2ee6b39ae71f3f76236007c35f5be1fbe3732a38aca98`  
		Last Modified: Thu, 17 Dec 2020 16:50:20 GMT  
		Size: 154.2 MB (154202254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:166bc6d0b07c05a8189e752f82ce51aa5c55648102f181154be68842357ecbaa`  
		Last Modified: Thu, 17 Dec 2020 16:49:49 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bd69f07c33ad7a8a34370173946d70c9cf63afdf20bb81c8793f7206564eca`  
		Last Modified: Thu, 17 Dec 2020 16:51:16 GMT  
		Size: 423.0 MB (422993028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
