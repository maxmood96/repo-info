## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:1304613324741ecacaeb549979b3e238ef6fef01335b12ed4483eb95df8729e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:728377205a2d449546fa1bae4ffedc4c6940a12f439e672ecb3381b0e3c290e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.3 MB (282343607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11b3dc1b02e8887c8d23f5d9be8f4300e135a96f9d4537804218ef1cbd5fe83`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:03:23 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:03:23 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:15:22 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 06 Nov 2025 22:15:22 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 06 Nov 2025 22:15:22 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 06 Nov 2025 22:15:22 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Thu, 06 Nov 2025 22:15:22 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Thu, 06 Nov 2025 22:15:22 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Thu, 06 Nov 2025 22:15:22 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Nov 2025 22:15:22 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Nov 2025 22:15:22 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:0936bd52c996ecee97f4dd53982e2e986383d631b1506cd33fb60fb70bef48bb`  
		Last Modified: Thu, 06 Nov 2025 07:20:38 GMT  
		Size: 62.9 MB (62934134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae7f1c4f823667d2bda7ac9bf9d583a2f705b6dd0847e7772d17fdcf1352183`  
		Last Modified: Thu, 06 Nov 2025 23:51:23 GMT  
		Size: 219.4 MB (219409473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:3d64b8b79fb4362a4d82bc6c3bd8da2e602065e6e56fed891356c166b3a5c860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1abfc66c949e6b6ff09268081538f4094baae3d282dfa2d1dd83a231999e3280`

```dockerfile
```

-	Layers:
	-	`sha256:a0b1bd3b56fdda83b6b817e4684f5b1c566e0566b33b2379fe4220215e7deefc`  
		Last Modified: Thu, 06 Nov 2025 23:48:47 GMT  
		Size: 5.1 MB (5082193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f9cf58414c03c4d4b43cf69291effb0cd4064df70d4185f42b2db96082c2284`  
		Last Modified: Thu, 06 Nov 2025 23:48:47 GMT  
		Size: 11.9 KB (11854 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:afc5a1821ed34c4c4af7cfc7b5e1540ddb5df4296e9e053dcfffefe24b1d04fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259697259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce0a872756a7e2ed80621780bf737645f215505db7e8f2791048f0175d67b12`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:02:17 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:02:17 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:15:02 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 06 Nov 2025 22:15:02 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 06 Nov 2025 22:15:02 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 06 Nov 2025 22:15:02 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Thu, 06 Nov 2025 22:15:02 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Thu, 06 Nov 2025 22:15:02 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Thu, 06 Nov 2025 22:15:02 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Nov 2025 22:15:02 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Nov 2025 22:15:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:a7c3aef254f38f8d9dc0b33a459e16cf71365801ec3cea141d9ae2909de17717`  
		Last Modified: Thu, 06 Nov 2025 03:12:00 GMT  
		Size: 64.8 MB (64793296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e492f8f736dbf1b8ea7de8e8a9dada9d16a282bbe7655eaaa9c79a7840c20c3d`  
		Last Modified: Thu, 06 Nov 2025 23:51:37 GMT  
		Size: 194.9 MB (194903963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:cabfa264933b65bf0a411abc54b74ca696b84e7b0dff999994672e889f7f7480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ef23520119fc01a5211d69ad761c757c38bf3c1bd70a0e39d55e1a635c4291`

```dockerfile
```

-	Layers:
	-	`sha256:e4d3af94ab267354c94ace212540515b86bec5f6a57b0929f01ebda7d166c004`  
		Last Modified: Thu, 06 Nov 2025 23:48:52 GMT  
		Size: 5.1 MB (5081627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91252b0747d4c3e00aba0bab4e4476398efdc4b3373b5c58517354c5e7a5daa1`  
		Last Modified: Thu, 06 Nov 2025 23:48:53 GMT  
		Size: 11.9 KB (11946 bytes)  
		MIME: application/vnd.in-toto+json
