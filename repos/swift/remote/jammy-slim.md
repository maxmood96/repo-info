## `swift:jammy-slim`

```console
$ docker pull swift@sha256:91232390bc204abcc2f3fa498cb44306ae53fa799b3190c0c385b0be2986ed84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:jammy-slim` - linux; amd64

```console
$ docker pull swift@sha256:3eadb6be97e9d5f79cb1e71261dc5b1c5a5d1353e47d27e2ba0f79e8f9e97555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97811201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0124cef719f3500f97b9f03635df1dfa4ddd3bae79fedd587d2bf4e7a0336b07`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Sat, 06 Sep 2025 05:03:28 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 06 Sep 2025 05:03:28 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 06 Sep 2025 05:03:28 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_BRANCH=swift-6.1.3-release
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_VERSION=swift-6.1.3-RELEASE
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 06 Sep 2025 05:03:28 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.1.3-release SWIFT_VERSION=swift-6.1.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 06 Sep 2025 05:03:28 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.1.3-release SWIFT_VERSION=swift-6.1.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b489538d928936f4a848c8e64540d870210212a209ef27afdf0bd84ca49ab2e5`  
		Last Modified: Mon, 08 Sep 2025 16:47:26 GMT  
		Size: 19.2 MB (19224061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24a05263ab3474e7957f4728ca06c15f547c48adab05b9fe50314607edc597d`  
		Last Modified: Mon, 08 Sep 2025 16:47:37 GMT  
		Size: 49.1 MB (49050205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy-slim` - unknown; unknown

```console
$ docker pull swift@sha256:a676fbe0c324ecb6b205702f16a661970f582a9d9bf914d8a74f1105a0df66b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3069462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dccd5e177ac8f26ab3c93cb1e3700348e5a0d61300ffbfa8879e603145861214`

```dockerfile
```

-	Layers:
	-	`sha256:b2a5c60e1865994946a7e2e77d0119f69bf0177d50327ceb1b3f54732a6e3d6f`  
		Last Modified: Mon, 08 Sep 2025 19:48:21 GMT  
		Size: 3.1 MB (3055479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fd129815afd11c4c8151e2ac069c87338c8cb906f38689618cac640d3c7e72b`  
		Last Modified: Mon, 08 Sep 2025 19:48:21 GMT  
		Size: 14.0 KB (13983 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:jammy-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:351650f86f2cc23733f3447629a2bb1d01b666039acdd4a9c98eb2740fc0a377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94844912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4362f6bed927fb89d84524b77e24ebd0229ccbb8e4c41958ea3155d63b00dfb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Sat, 06 Sep 2025 05:03:28 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 06 Sep 2025 05:03:28 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 06 Sep 2025 05:03:28 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_BRANCH=swift-6.1.3-release
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_VERSION=swift-6.1.3-RELEASE
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 06 Sep 2025 05:03:28 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.1.3-release SWIFT_VERSION=swift-6.1.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 06 Sep 2025 05:03:28 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.1.3-release SWIFT_VERSION=swift-6.1.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a6be407cdce3afd7ba72498fe7b690c90da3e045e2c7ca0ea5c0de7ae9b12d`  
		Last Modified: Mon, 08 Sep 2025 16:49:06 GMT  
		Size: 19.1 MB (19088891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8735aeac7737f7a316db5298ad792b239567c5bda91166f3ac799d28694b4bed`  
		Last Modified: Mon, 08 Sep 2025 16:49:11 GMT  
		Size: 48.4 MB (48394552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy-slim` - unknown; unknown

```console
$ docker pull swift@sha256:4bb30698a51f83f8d91c56d728d21d14e0f78fb637c54e9e0add5c2971ed967c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3069856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764a86e4b4ed429c1663ed345742aa4b0892b752223b07a9bd1abd25a17d1ccd`

```dockerfile
```

-	Layers:
	-	`sha256:d11923f8e063f50f82a608be90c1e5d862cea7d36d2790c189a6e7d24942adc2`  
		Last Modified: Mon, 08 Sep 2025 19:48:26 GMT  
		Size: 3.1 MB (3055766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce724581c3a49484753abf645aab7f4a5c89e0935598d19adb61888289448e41`  
		Last Modified: Mon, 08 Sep 2025 19:48:27 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json
