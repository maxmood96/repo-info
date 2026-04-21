## `swift:amazonlinux2023-slim`

```console
$ docker pull swift@sha256:6d02ad6079c26084462bb953d38c36c36667b9d16f65b0dcc2c8c87c147b78df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2023-slim` - linux; amd64

```console
$ docker pull swift@sha256:93473564467b8c17be689f40a3ac018e0b803cc10ce2f54b841016e756dc6501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.7 MB (245652043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:132e469bae413a5431e73e69180a354b5fd0a204d4898eb715a37c4d10d5dff4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 21:53:10 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 20 Apr 2026 21:53:10 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 20 Apr 2026 21:53:10 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 20 Apr 2026 21:53:10 GMT
ARG SWIFT_PLATFORM=amazonlinux2023
# Mon, 20 Apr 2026 21:53:10 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Mon, 20 Apr 2026 21:53:10 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Mon, 20 Apr 2026 21:53:10 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 20 Apr 2026 21:53:10 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 20 Apr 2026 21:53:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN dnf -y swap gnupg2-minimal gnupg2-full # buildkit
# Mon, 20 Apr 2026 21:53:44 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && dnf -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587f2973102cf5ac7ddd3b245048f80e82df66a0312409656cca47a2e6bad866`  
		Last Modified: Mon, 20 Apr 2026 21:54:04 GMT  
		Size: 136.3 MB (136263037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2920e0d3fd561b49cebf046a5b81a5ef75f993ed2b950c3649ebd6cb0fb9f3`  
		Last Modified: Mon, 20 Apr 2026 21:54:02 GMT  
		Size: 54.8 MB (54817752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2023-slim` - unknown; unknown

```console
$ docker pull swift@sha256:34c25626710509c2d463d4ae87b74867e4e89731a59788ed43908c7bb64a0004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6465686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f4b2207b0847078c3157b558944654c774428dc8f6169b428fbf24ab5afafb`

```dockerfile
```

-	Layers:
	-	`sha256:956ed0f0fb4db4ffed4c89087e762cdcbb787e242f96010e6925d896550799dc`  
		Last Modified: Mon, 20 Apr 2026 21:54:00 GMT  
		Size: 6.5 MB (6452556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e808cb31ce281dae10521ae0bc2f3286a5e524eda44872f61be11cec12b997e`  
		Last Modified: Mon, 20 Apr 2026 21:54:00 GMT  
		Size: 13.1 KB (13130 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2023-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:6ba0eac7919feb4bf2f04dd0f83e80d7c1f3721511bfea88d67938685cec695e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.7 MB (242737690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcd9ee2ae233ba5d804dca32b65337876e674ab03915f5bc91c378e13550ab9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 22:00:11 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 20 Apr 2026 22:00:11 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 20 Apr 2026 22:00:11 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 20 Apr 2026 22:00:11 GMT
ARG SWIFT_PLATFORM=amazonlinux2023
# Mon, 20 Apr 2026 22:00:11 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Mon, 20 Apr 2026 22:00:11 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Mon, 20 Apr 2026 22:00:11 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 20 Apr 2026 22:00:11 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 20 Apr 2026 22:00:11 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN dnf -y swap gnupg2-minimal gnupg2-full # buildkit
# Mon, 20 Apr 2026 22:00:54 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && dnf -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0354fcd7cfebce8bc8878fe98d311fdda2f5bd1a8848f21a0358e4938a9c860`  
		Last Modified: Mon, 20 Apr 2026 22:01:16 GMT  
		Size: 135.1 MB (135068378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b27f95005d606a83b3e54765bab370aa7456ef0a472a212c7aac65ab7c7d560`  
		Last Modified: Mon, 20 Apr 2026 22:01:15 GMT  
		Size: 54.2 MB (54226573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2023-slim` - unknown; unknown

```console
$ docker pull swift@sha256:0753fe0b7e2cbc8f9ca5b5248af30a523d1595c658fb59f261bed21ebbf4bd9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6465300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9347f2da0c4798aa2bd3cddcbd894792aad0514a76b71d4b0fd147d16e4703bf`

```dockerfile
```

-	Layers:
	-	`sha256:05e407c402f0dc0e411689c312049e8d533859b8000c03873e3ee11887db6615`  
		Last Modified: Mon, 20 Apr 2026 22:01:13 GMT  
		Size: 6.5 MB (6452063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ca47611a674587590161f9b0a55296cf8d07ca0f089cb29e542a4a60646234d`  
		Last Modified: Mon, 20 Apr 2026 22:01:15 GMT  
		Size: 13.2 KB (13237 bytes)  
		MIME: application/vnd.in-toto+json
